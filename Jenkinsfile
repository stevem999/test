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
        nexusArtifactUploader artifacts: [[artifactId: 'test.txt', classifier: '', file: 'test.txt', type: 'Text']], credentialsId: '', groupId: 'testGroups', nexusUrl: 'localhost:8081', nexusVersion: 'nexus3', protocol: 'https', repository: 'testRawRepoLocal', version: 'testVersion1.2.3'
      }
    }
  }
  environment {
    testEnv = 'local'
  }
}
