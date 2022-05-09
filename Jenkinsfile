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
            echo "Get the driver path ${ChromeDriverPath}}"
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