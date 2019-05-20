pipeline {
  agent any
 
  tools {nodejs "node-lts"}
  environment {
    SECRET = credentials('jenkins-secret')
    PUBLIC = 'a public text'
  }
 
  stages {
    stage('Install') {
      steps {
        sh 'npm install'
      }
    }
    stage('Build') {
      steps {
        sh 'npm run build'
      }
    }
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo $SECRET'
        sh 'echo $PUBLIC'
      }
    }
  }
}