pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'test11'
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
            echo 'test22'
          }
        }
      }
    }
  }
}