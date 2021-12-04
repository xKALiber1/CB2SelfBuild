pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build Java 7 theoretical') {
          agent any
          steps {
            echo 'Build Build Build Build'
          }
        }

        stage('Build Java 8 theoretical') {
          agent any
          environment {
            BUILD_NAME = 'theoretical java 8 build'
          }
          steps {
            echo 'here I would have a shell script that echos I am a $BUZZ _NAME! and then ./jenkins/build.sh which would be the file of the build'
          }
        }

      }
    }

    stage('Test A') {
      parallel {
        stage('Test') {
          steps {
            echo 'echo I\'m glad it worked but hopefully this will test out and deploy'
            echo 'i would here have a node for build java 7 had i had the option under the node selection from cloud bees this way the build would be tested and run on this node'
          }
        }

        stage('Test B') {
          steps {
            sh 'echo it worked and this is from CLI but delayed for 5'
            echo 'i would here have a node for build java 8 had i had the option under the node selection from cloud bees this way the build would be tested and run on this node'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'echo deployed in theory from the CLI'
      }
    }

  }
}