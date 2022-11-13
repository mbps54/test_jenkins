pipeline {
  agent none
  parameters {
    string(name: 'DEPLOY_ENV', defaultValue: 'staging', description: '')
  }
  stages {
    stage ('Deploy'){
      steps {
      echo "Deploying to ${DEPLOY_ENV}"
      }
    }
  }
}
