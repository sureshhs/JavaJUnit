pipeline {
	agent any
	
	    tools {
        		maven 'MyMaven' 
		    	jdk 'JDK'
    		}
	stages {
			stage ('Compile stage') {
					steps {
							bat 'mvn clean compile'
					}
			}
			stage ('Run test stage') {
					steps {
							bat 'mvn test'
					}
			}		
	}
	
	post {
		success {
			mail to: "sureshhs@hotmail.com",
			subject: "SUCCESSFUL: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]' (${env.BUILD_URL})",
			body: "This email from Jenkins pipeline"		
		}
		unstable {
			mail to: "sureshhs@hotmail.com",
			subject: "UNSTABLE: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]' (${env.BUILD_URL})",
			body: "This email from Jenkins pipeline"	
		}
		failure {
			mail to: "sureshhs@hotmail.com",
			subject: "FAILED: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]' (${env.BUILD_URL})",
			body: "This email from Jenkins pipeline"
		}	
	}
}				
