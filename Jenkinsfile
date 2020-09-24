pipeline {
	tools{
        jdk 'myjava'
        maven 'mymaven'
    }
	agent any
	stages {
		stage ('Checkout') {
			steps{
			git 'https://github.com/vidyasagarkolusu/cicdpipelines.git'
			}
		}
		stage ('Build') {
			steps {
			echo "from Build Stage"
			//sh "mvn -f ${jenkins_ws}/${JOB_NAME}//pom.xml  clean install"
			}
		}
	}
}
