pipeline{
	agent any
	stages{
		stage('Build'){
			step{
				sh 'mvn clean package-pipeline'
			}
			post{
				success{
					echo 'Now Archiving...'
					archiveArtifacts artifacts: '**/target/*.war'
				}
			}
		}
	}
}
