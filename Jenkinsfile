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
cypress --help
cypress -v
cypress run --config-file ./cypress.config.js
'''
      }
    }

  }
}