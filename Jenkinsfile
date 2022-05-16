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

  }
}