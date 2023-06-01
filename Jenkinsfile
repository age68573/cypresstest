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
        sh 'npm run cy:run -- --record --config-file "./cypress.config.js" --spec "cypress/e2e/spec.cy.js"'
      }
    }

  }
}