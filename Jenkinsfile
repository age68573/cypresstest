pipeline {
  agent none
  stages {
    stage('cypress') {
      agent {
        docker {
          image 'cypress/included'
        }

      }
      steps {
        sh '''npm ci
npm run cy:run  --spec "cypress/e2e/spec.cy.js"'''
      }
    }

  }
}