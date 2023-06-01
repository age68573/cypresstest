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
        sh 'echo npm -v'
      }
    }

  }
}