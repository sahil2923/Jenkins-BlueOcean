pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'ls'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'test message'
          }
        }

        stage('Test prod') {
          steps {
            echo 'testprod'
            sleep 10
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'production done'
      }
    }

  }
}
