pipeline{
	agent any
	tools{
		maven 'LocalMAVEN'
	}
	stages{
		stage('Build'){
			steps{
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
