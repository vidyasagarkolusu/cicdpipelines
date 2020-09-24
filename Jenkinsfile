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
			sh "mvn -f /var/lib/jenkins/workspace/job1/pom.xml package"
			}
		}
	}
}
