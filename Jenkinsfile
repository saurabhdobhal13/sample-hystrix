pipeline{
	agent any 
		stages {
			stage('Compile Stage') {
				steps {
					withMaven(maven: 'mvn') {
					sh 'mvn clean compile'
					}
				}
				
			stage('Testing Stage') {
				steps {
					withMaven(maven: 'mvn') {
					sh 'mvn test'
					}
				}
			stage('Deploying Stage') {
				steps {
					withMaven(maven: 'mvn') {
					sh 'mvn deploy'
					}
				}
			}
	
		}
}