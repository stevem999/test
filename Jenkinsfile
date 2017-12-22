pipeline {
  agent any
  stages {
    stage('TestStage') {
      steps {
        sleep 1
        echo 'test message'
        fileExists 'test.txt'
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
