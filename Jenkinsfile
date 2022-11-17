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
          sh "npm install"
        }
      }
    }
    stage('test') {
      steps {
        nodejs('nodejs8') {
          sh "npm test"
        }
      }
    }
  }
}
