pipeline{
	agent any 
	  tools {
        maven "maven-3.6.3"
    	}
		stages {
			stage('Compile Stage') {
				steps {
					withMaven(maven: 'maven-3.6.3') {
					sh 'mvn clean compile'
					}
				}
			}
				
			stage('Testing Stage') {
				steps {
					withMaven(maven: 'maven-3.6.3') {
					sh 'mvn test'
					}
				}
			}
			stage('Deploying Stage') {
				steps {
					withMaven(maven: 'maven-3.6.3') {
					sh 'mvn deploy'
					}
				}
			}
	
		}
}