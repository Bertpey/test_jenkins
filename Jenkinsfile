pipeline {
  agent any
  stages {
    stage('Buzz Build') {
      parallel {
        stage('Buzz Build') {
          steps {
            sh './scripts/run_all.sh'
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