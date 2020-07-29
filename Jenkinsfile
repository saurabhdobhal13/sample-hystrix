pipeline{
	agent any 
		stages {
			stage('Compile Stage') {
				steps {
					def mvn_version = 'maven-3.6.3'
					withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] ) {	
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