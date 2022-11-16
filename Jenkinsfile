pipeline {
  agent any
  stages {
    stage('pre check') {
      steps {
        sh '''ping 8.8.8.8 -c 2
ping 1.1.1.1 -c 2'''
        sh 'ping 9.9.9.9 -c 2'
        sh 'echo "ping tests are completed, data is collected"'
      }
    }

    stage('configuration') {
      steps {
        sh 'echo "do you job here"'
      }
    }

    stage('post check') {
      steps {
        sh 'ping 8.8.8.8 -c 2'
        sh 'echo "result is here"'
      }
    }

  }
  environment {
    env1 = 'Moon'
  }
}