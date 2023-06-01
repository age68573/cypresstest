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
          image 'cypress/included'
        }

      }
      steps {
        sh '''npm ci

npm run cy:run  --spec "cypress/e2e/my-spec.cy.js"'''
      }
    }

  }
}