pipeline {
	agent any
	
	    tools {
        		maven 'MyMaven' 
    		}
	stages {
			stage ('Compile stage') {
					steps {
							sh 'mvn clean compile'
					}
			}
			stage ('Run test stage') {
					steps {
							sh 'mvn test'
					}
			}	
			stage ('Deploy stage') {
					steps {
							sh 'mvn deploy'
					}							
			}		
	}
}				
