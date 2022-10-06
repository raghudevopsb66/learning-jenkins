pipeline {
  agent {
    node { label 'workstation' }
  }

  options { disableConcurrentBuilds() }

  environment {
    SAMPLE_URL = "google.com"
    SSH = credentials('SSH')
  }

  //triggers { pollSCM('* * * * *') }

  tools {
    maven 'MAVEN'
  }

  parameters {
    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
    booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
    choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
    password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
  }

  stages {
    stage('Hello') {
      steps {
        echo 'Hello World'
        echo "URL = ${SAMPLE_URL}"
        echo "${SSH}"
        echo "PERSON = ${PERSON}"
        sh 'mvn --version'
      }
    }

    stage('Hello1') {
      input {
        message "Should we continue?"
        ok "Yes, we should."
        submitter "alice,bob"
        parameters {
          string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        }
      }
      steps {
        echo "PERSON = ${PERSON}"
      }
    }

  }

  post {
    always {
      echo 'I will always say Hello again!'
    }
  }

}


