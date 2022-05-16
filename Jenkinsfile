pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        chuckNorris()
      }
    }

    stage('clean install') {
      steps {
        build 'clean'
      }
    }

  }
}