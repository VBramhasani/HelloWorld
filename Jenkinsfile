pipeline {
    node('WinAgent') {
    stage('scm checkout'){
		git 'https://github.com/VBramhasani/HelloWorld.git'
	}
	stage('compile-package'){
		sh 'mvn clean package'
	}
    }
}
