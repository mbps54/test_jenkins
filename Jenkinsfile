pipeline {
  agent any
  parameters {
    string(name: 'DEPLOY_ENV', defaultValue: 'staging', description: '')
  }
  stages {
    stage('stage  1') {
      steps {
        sh 'echo "hello stage 1 step 1 modified" > file.txt'
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
        input(message: 'Deploy to Stage', ok: 'Yes')
        sh 'echo hello stage 3 step 1'
      }
    }
    stage('archiveartifacts') {
      steps {
        archiveArtifacts(artifacts: 'file.txt', fingerprint: true)
      }
    }
  }
}
