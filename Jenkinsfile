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
            echo "Get the driver path ${ChromeDriverPath}"
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying the app'
        input(message: 'Do you want to procced with Deployment', id: 'OK')
      }
    }

  }
  environment {
    ChromeDriverPath = 'E:\\chromedriver'
  }
}