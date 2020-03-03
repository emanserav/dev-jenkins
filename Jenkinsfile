pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building ...'
      }
    }

    stage('Test 1') {
      parallel {
        stage('Test 1') {
          steps {
            sh 'echo \'Perform Testing #1 ...\''
          }
        }

        stage('Test 2') {
          steps {
            sh 'echo \' Perform Testing 2 ...\'; exit 1'
          }
        }

        stage('Test 3') {
          steps {
            sh 'echo \'Perform Testing 3 ...\''
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying ...'
      }
    }

  }
}
