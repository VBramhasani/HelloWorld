pipeline{
	agent {
		label 'WinAgent'
	}	
	stages{
		stage('Clean'){
			steps{
				bat 'mvn clean'
			}
		}
		stage('Test'){
			steps{
				bat "mvn test"
			}
		}
		stage('package') {
			steps {
				bat "mvn package"
				}
		}
		stage('upload Artifactory'){
			steps{
			nexusVersion: 'nexus 2',
			protocol: 'http',
			nexusUrl: 'http://localhost:8081/nexus/content/repositories/Myrepo/',
			groupId: 'my.company',
			version: 1.0,
			repository: 'releases',
			credentialsId: 'Nexuscredentials',
			artifacts: [
			[artifactId: HelloWorld,
			classifier: '',
			file: 'HelloWorld-' + 1.0 + '.jar',
			type: 'jar']]
			
			}
		}
	}
}
