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
			stage ('Deploy stage') {
					steps {
							bat 'mvn deploy'
					}							
			}		
	}
}				
