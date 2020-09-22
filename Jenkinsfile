pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'This is build stage'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'This is Test stage'
          }
        }

        stage('int test') {
          steps {
            sh '''echo "This is int test"
df -h'''
          }
        }

        stage('load test') {
          steps {
            sh '''echo "This is load test"
ip addr
ip route'''
          }
        }

      }
    }

    stage('Deploy') {
      { 
        when branch 'master'
      }
      steps {
        echo 'This is deploy stage'
      }
    }

  }
}
