pipeline{
	agent{
		label: WinAgent
		}
	Stages{
		stage('SCM Checkout'){
			git 'https://github.com/VBramhasani/HelloWorld.git'
		}
		stage('build'){
			sh 'mvn clean package'
		}
	}
	post {
        always {
            archiveArtifacts '**/*.jar'
        }
		}
	}
