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
          args ' -v $PWD:/e2e -w /e2e  --spec ./cypress/e2e/spec.cy.js'
        }

      }
      steps {
        sh '''npm -v
echo $NODE_PATH
ls -a
echo $(npm bin)
cypress --help
cypress -v
cypress verify
cypress info
cypress run --config-file ./cypress.config.js
'''
      }
    }

  }
}