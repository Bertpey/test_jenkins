pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        chuckNorris()
      }
    }

    stage('message') {
      steps {
        echo 'bzee bzee'
      }
    }

    stage('Bees Bees') {
      steps {
        echo 'Bees Bees'
      }
    }

    stage('test shell') {
      steps {
        sh 'mvn clean install'
      }
    }

  }
}