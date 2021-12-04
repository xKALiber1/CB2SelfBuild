pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build Build Build Build'
      }
    }

    stage('Test A') {
      parallel {
        stage('Test') {
          steps {
            echo 'echo I\'m glad it worked but hopefully this will test out and deploy'
          }
        }

        stage('Test B') {
          steps {
            sh 'echo it worked and this is from CLI but delayed for 5'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'echo I\'m glad it worked but hopefully this will deploy'
      }
    }

  }
}