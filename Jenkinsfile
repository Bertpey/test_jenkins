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

    stage('test input') {
      when {
        equals expected: 'Fred', actual: "${PERSON}"
      }
      input {
        message 'Should we continue?'
        id 'Yes, we should.'
        submitter 'alice,bob'
        parameters {
          string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I greet?')
        }
      }
      steps {
        echo "Hello, ${PERSON}, nice to meet you."
      }
    }

  }
  post {
    always {
      echo 'I will always say Hello again!'
    }

  }
}