pipeline {
	agent any
	stages {
		stage ('Checkout') {
		checkout([$class: 'GitSCM', 
    branches: [[name: '*/master']], 
    doGenerateSubmoduleConfigurations: false, 
    extensions: [[$class: 'CleanCheckout']], 
    submoduleCfg: [], 
    userRemoteConfigs: [[credentialsId: 'git-credentials', url: 'https://github.com/devops-trainer/DevOpsClassCodes.git']]
])
		}
		stage ('Build') {
			echo "from Build Stage"
			//sh "mvn -f ${jenkins_ws}/${JOB_NAME}//pom.xml  clean install"
		}
	}
}
