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

        stage('Test Log') {
          steps {
            writeFile(file: 'testlog.txt', text: 'this is automation log')
          }
        }

      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy') {
          steps {
            input(message: 'Do you want to procced with Deployment?', id: 'OK')
            echo 'Deploying the app'
          }
        }

        stage('Artifcats') {
          steps {
            archiveArtifacts 'testlog.txt'
          }
        }

      }
    }

  }
  environment {
    ChromeDriverPath = 'E:\\chromedriver'
  }
}