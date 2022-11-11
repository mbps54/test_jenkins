pipeline {
  agent any
  stages {
    stage('stage 1') {
      steps {
        sh 'echo hello stage 1 step 1'
      }
    }
    stage(' stage 2') {
      parallel {
        stage('parrarel 1') {
          steps {
            sh 'echo hello stage 2 step 1'
          }
        }
        stage('parrarel 2') {
          steps {
            sh 'echo hello stage 2 step 2'
          }
        }
        stage('parrarel 3') {
          steps {
            sh 'echo hello stage 2 step 3'
          }
        }
        stage('parrarel 4') {
          steps {
            sh 'echo hello stage 2 step 4'
          }
        }
      }
    }
    stage('stage 3') {
      steps {
        sh 'echo hello stage 3 step 1'
      }
    }
  }
}
