pipeline {
  agent any
  stages {
    stage('Buzz Build') {
      parallel {
        stage('Buzz Build') {
          steps {
            sh '''sleep 5
echo done.'''
          }
        }

        stage('buzz2') {
          steps {
            sh '''sleep 10
echo done.'''
          }
        }

      }
    }

    stage('test') {
      steps {
        input(message: 'test ?', ok: 'ok')
      }
    }

  }
  post {
    always {
      echo 'I will always say Hello again!'
    }

  }
}