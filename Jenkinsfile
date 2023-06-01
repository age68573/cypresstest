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

npm run cy:run  --spec "cypress/e2e/my-spec.cy.js"'''
      }
    }

  }
}