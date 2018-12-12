pipeline{
	agentt {
		label 'WinAgent'
	}	
	stages{
		stage('Clean'){
			steps{
				sh 'mvn clean'
			}
		}
		stage(Maven Test){
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
