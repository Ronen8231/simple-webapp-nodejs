pipeline {
    agent any
    stages {
        stage("Initialize") {
            steps {
		sh "ls"
                //cleanWs()
            }
        }
	stage('build') {
	steps {
	   nodejs('nodejs8') {
		npm install
           }
	}
	}
    }	
}
