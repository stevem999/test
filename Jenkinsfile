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
        mail(subject: 'TestSubject', body: 'TestBody', from: 'jenkins', to: 'steeve.mercier@gmail.com')
      }
    }
  }
  environment {
    testEnv = 'local'
  }
}