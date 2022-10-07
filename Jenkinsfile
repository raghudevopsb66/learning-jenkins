//pipeline {
//  agent {
//    node { label 'workstation' }
//  }
//
//  options { disableConcurrentBuilds() }
//
//  environment {
//    SAMPLE_URL = "google.com"
//    SSH = credentials('SSH')
//  }
//
//  //triggers { pollSCM('* * * * *') }
//
//  tools {
//    maven 'MAVEN'
//  }
//
//  parameters {
//    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
//    text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
//    booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
//    choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
//    password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
//  }
//
//  stages {
//    stage('Hello') {
//      steps {
//        echo 'Hello World'
//        echo "URL = ${SAMPLE_URL}"
//        echo "${SSH}"
//        echo "PERSON = ${PERSON}"
//        sh 'mvn --version'
//      }
//    }
//
//    stage('Hello1') {
//      input {
//        message "Should we continue?"
//        ok "YES"
//        submitter "admin"
//      }
//      steps {
//        echo "PERSON = ${PERSON}"
//      }
//    }
//
//  }
//
//  post {
//    always {
//      echo 'I will always say Hello again!'
//    }
//  }
//
//}
//
//

//pipeline {
//  agent any
//
//  parameters {
//    choice(name: 'DEPLOY_TO', choices: ['', 'DEV', 'PROD'], description: 'Pick ENv')
//  }
//
//  stages {
//
//    stage('DEV') {
//      when {
//        environment name: 'DEPLOY_TO', value: 'DEV'
//        //expression { COUNT > 1 }
//        //IS_TRUE   // IS_TRUE is a boolean and condition is true if the input is true
//      }
//      steps {
//        echo 'One'
//      }
//    }
//
//    stage('PROD') {
//      when {
//        environment name: 'DEPLOY_TO', value: 'PROD'
//      }
//      steps {
//        echo 'Two'
//      }
//    }
//
//  }
//
//}

//pipeline {
//  agent any
//
//  parameters {
//    booleanParam(name: 'DEPLOY', defaultValue: true, description: 'DEPLOY ?')
//  }
//
//  stages {
//
//    stage('DEV') {
//      when {
//        expression {
//          return params.DEPLOY
//        }
//
//      }
//      steps {
//        echo 'One'
//      }
//    }
//
//
//  }
//
//}


pipeline {
  agent any

  stages {

    stage('Parallel Stages') {
      parallel {
        stage('Stage1') {
          steps {
            echo 'one'
          }
        }
        stage('Stage2') {
          steps {
            echo 'one'
          }
        }
        stage('Stage3') {
          steps {
            echo 'one'
          }
        }
        stage('Stage4') {
          steps {
            echo 'one'
          }
        }
      }
    }

    stage('Two') {
      steps {
        echo 'two'
      }
    }
    stage('Three') {
      steps {
        echo 'three'
      }
    }


  }

}
