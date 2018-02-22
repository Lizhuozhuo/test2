pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo \'hello\''
      }
    }
    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'test'
          }
        }
        stage('error') {
          steps {
            sh 'echo \'world\''
          }
        }
      }
    }
  }
}