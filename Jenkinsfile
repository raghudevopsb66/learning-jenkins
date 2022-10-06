pipeline {
  agent {
    node { label 'workstation' }
  }

  stages {
    stage('Hello') {
      steps {
        echo 'Hello World'
      }
    }
  }

  post {
    always {
      echo 'I will always say Hello again!'
    }
  }

}

