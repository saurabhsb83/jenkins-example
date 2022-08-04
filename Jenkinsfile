

pipeline {
	agent any 
	
	stages {
			stage ('Compile Stage')  {
					steps {
					withMaven(maven : 'MAVEN36' ) {
						bat 'mvn clean compile'
					}
					
					}
			}
			
			stage ('Testing Stage') {
				steps {
						withMaven( maven : 'MAVEN36' ) {
							bat 'mvn test'
						}
				}
			}
			
			
			stage('Deployment Stage') {
				steps {
				
				withMaven(maven : 'MAVEN36') {
					bat 'mvn install'
				}
			}
		}
	}
}
