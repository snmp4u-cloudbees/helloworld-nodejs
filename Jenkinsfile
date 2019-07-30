pipeline {
  agent none
  options { 
    buildDiscarder(logRotator(numToKeepStr: '2'))
    skipDefaultCheckout true
  }
  stages {
    stage('Test') {     
      agent { label 'nodejs-app' }
      steps {
        checkout scm
        container('nodejs') {
          echo 'checkout scm'
          echo 'Hello World!'   
          sh 'node --version'
        }
      }
    }             
  }
}
  
