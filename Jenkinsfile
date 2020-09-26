pipeline {
	tools{
        jdk 'myjava'
        maven 'mymaven'
    }
	agent any
	stages {
		stage ('Checkout') {
			steps{
			git 'https://github.com/devops-trainer/DevOpsClassCodes.git'
			}
		}
		stage ('Build') {
			steps {
			echo "from Build Stage"
			sh "mvn -f /var/lib/jenkins/workspace/Pip-01/pom.xml package"
			}
		}
		stage('Sonarqube') {
    environment {
        scannerHome = tool 'SonarQubeScanner'
    }
    steps {
        withSonarQubeEnv('SonarQubeServer') {
            sh "${scannerHome}/bin/sonar-scanner -Dsonar.host.ur=http://3.7.66.233:9000/ -Dsonar.projectKey=${JOB_NAME} -Dsonar.projectName=${JOB_NAME} -Dsonar.sources=/var/lib/jenkins/workspace/Pip-01/src -Dsonar.java.binaries=/var/lib/jenkins/workspace/Pip-01/target/"
        }
       // timeout(time: 10, unit: 'MINUTES') {
          //  waitForQualityGate abortPipeline: true
        // }
    }
}
	}
}
