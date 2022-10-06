pipeline {
  agent {
    node { label 'workstation' }
  }

  options { disableConcurrentBuilds() }

  environment {
    SAMPLE_URL = "google.com"
    SSH = credentials('SSH')
  }

  stages {
    stage('Hello') {
      steps {
        echo 'Hello World'
        echo "URL = ${SAMPLE_URL}"
        echo "${SSH}"
      }
    }
  }

  post {
    always {
      echo 'I will always say Hello again!'
    }
  }

}

