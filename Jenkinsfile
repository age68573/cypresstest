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
        sh '''npm -v
echo $NODE_PATH
ls -a
echo $(npm bin)
${NODE_PATH}/.bin/cypress run --config-file ./cypress.config.js
'''
      }
    }

  }
}