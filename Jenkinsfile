pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('Checkout Codebase'){
        steps{
            checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github', url: 'https://github.com/age68573/cypresstest.git']])
        }
    }
    stage('cypress') {
      steps {
        sh ' docker run  -v $PWD:/e2e -w /e2e  cypress/included --spec ./cypress/e2e/spec.cy.js'
      }
    }

  }
}
