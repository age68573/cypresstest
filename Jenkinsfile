pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('cypress') {
      steps {
        sh 'docker run  -v $PWD:/e2e -w /e2e  cypress/included --spec ./cypress/e2e/spec.cy.js'
      }
    }

  }
}