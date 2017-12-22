pipeline {
  agent any
  stages {
    stage('TestStage') {
      steps {
        sleep 1
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