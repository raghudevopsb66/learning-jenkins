pipeline {
  agent {
    node { label 'workstation' }
  }

  environment {
    SAMPLE_URL = "google.com"
  }

  stages {
    stage('Hello') {
      steps {
        echo 'Hello World'
        echo "URL = ${SAMPLE_URL}"
      }
    }
  }

  post {
    always {
      echo 'I will always say Hello again!'
    }
  }

}

