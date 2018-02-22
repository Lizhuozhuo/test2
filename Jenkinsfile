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
            sleep(time: 1, unit: 'MINUTES')
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