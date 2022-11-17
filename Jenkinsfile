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
        //nodejs('nodejs8') {
          //sh "npm install"
        //}
        sh "docker build -t nodewebapp ."
	sh "docker images"
        sh "docker ps"
      }
    }
    //stage('test') {
    //  steps {
    //    nodejs('nodejs8') {
    //      sh "npm test"
    //    }
    //  }
   // }
     stage('deploy') {
        steps {
           sh "docker run -itd --name nodewebapp -p 3000:3000 nodewebapp:latest"
        }
     }
  }
}
