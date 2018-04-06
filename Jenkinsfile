pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
    stage('Deliver') {
      steps {
        sh 'npm start &'
        sh 'sleep 1'
        sh 'killall -9 node'
      }
    }
  }
  environment {
    CI = 'true'
  }
}