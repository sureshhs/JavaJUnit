pipeline {
	agent any
	
	stages {
			stage ('Compile stage') {
					steps {
						withMaven(maven : 'MyMaven') {
							sh 'mvn clean compile'
						}					
					}
			}
			stage ('Run test stage') {
					steps {
						withMaven(maven : 'MyMaven') {
							sh 'mvn test'
						}					
					}
			}	
			stage ('Deploy stage') {
					steps {
						withMaven(maven : 'MyMaven') {
							sh 'mvn deploy'
						}					
					}							
			}		
	}
}				
