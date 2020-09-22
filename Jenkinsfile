pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        retry(count: 1)
        sh 'echo "Hi this is build stage"'
        echo 'This is build stage'
      }
    }

    stage('Test') {
      steps {
        echo 'This is Test stage'
      }
    }

    stage('Deploy') {
      steps {
        echo 'This is deploy stage'
      }
    }

  }
}