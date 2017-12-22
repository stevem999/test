pipeline {
  agent any
  stages {
    stage('TestStage') {
      parallel {
        stage('TestStage') {
          steps {
            sleep 1
            echo 'test message'
            fileExists 'test.txt'
          }
        }
        stage('test parallel') {
          steps {
            sleep 1
          }
        }
      }
    }
    stage('Build Code') {
      steps {
        echo 'test message'
        fileExists 'test.txt'
      }
    }
  }
  environment {
    testEnv = 'local'
  }
}