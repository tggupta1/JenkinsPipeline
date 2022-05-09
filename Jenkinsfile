pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Build Application'
          }
        }

        stage('Test') {
          steps {
            echo 'Test the application'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying the app'
      }
    }

  }
}