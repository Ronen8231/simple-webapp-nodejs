pipeline {
  agent any
  options {
    skipDefaultCheckout()
  }
  stages {
    stage("Initialize") {
      steps {
        cleanWs()
        checkout scm
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

