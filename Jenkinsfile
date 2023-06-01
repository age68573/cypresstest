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
npm cypress install
ls
echo $(npm bin)
cypress run --config-file ./cypress.config.js
'''
      }
    }

  }
}