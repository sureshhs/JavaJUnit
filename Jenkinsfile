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
			subject: "${currentBuild.FullDisplayName} Maven build succeeded",
			body: "This email from Jenkins pipeline"		
		}
		unstable {
			mail to: "sureshhs@hotmail.com",
			subject: "${currentBuild.FullDisplayName} Maven build is unstable",
			body: "This email from Jenkins pipeline"	
		}
		failure {
			mail to: "sureshhs@hotmail.com",
			subject: "${currentBuild.FullDisplayName} Maven build failed",
			body: "This email from Jenkins pipeline"
		}	
	}
}				
