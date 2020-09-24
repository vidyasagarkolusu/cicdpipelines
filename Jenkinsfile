pipeline {
	tools{
        jdk 'java'
        maven 'Mymaven'
    }
	agent any
	stages {
		stage ('Checkout') {
			git 'https://github.com/vidyasagarkolusu/cicdpipelines.git'
		}
		stage ('Build') {
			echo "from Build Stage"
			//sh "mvn -f ${jenkins_ws}/${JOB_NAME}//pom.xml  clean install"
		}
	}
}
