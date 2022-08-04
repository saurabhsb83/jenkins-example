

pipeline {
	agent any 
	
	stages {
			stage ('Compile Stage')  {
					steps {
					withMaven(maven : 'MAVEN36' ) {
						sh 'mvn clean compile'
					}
					
					}
			}
			
			stage ('Testing Stage') {
				steps {
						withMaven( maven : 'MAVEN36' ) {
							sh 'mvn test'
						}
				}
			}
			
			
			stage('Deployment Stage') {
				steps {
				
				withMaven(maven : 'MAVEN36') {
					sh 'mvn install'
				}
			}
		}
	}
}
