pipeline{
	agent {
		label 'WinAgent'
	}	
	stages{
		stage('Clean'){
			steps{
				sh 'mvn clean'
			}
		}
		stage('Test'){
			steps{
				sh "mvn test"
			}
		}
		stage('package') {
			steps {
				sh "mvn package"
				}
			}
		
	}
}
