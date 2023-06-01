pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('cypress') {
      agent {
        docker {
          image 'cypress/base:18.14.1'
        }

      }
      steps {
        sh '''npm ci
npm run test:ci:record'''
      }
    }

  }
}