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
			subject: "${currentBuild.FullDisplayName} Maven build succeeded"	
		}
		unstable {
			mail to: "sureshhs@hotmail.com",
			subject: "${currentBuild.FullDisplayName} Maven build is unstable"	
		}
		failure {
			mail to: "sureshhs@hotmail.com",
			subject: "${currentBuild.FullDisplayName} Maven build failed"	
		}	
	}
}				
