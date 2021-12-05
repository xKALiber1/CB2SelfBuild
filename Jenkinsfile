pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build Java 7 theoretical') {
          agent any
          steps {
            echo 'Build Build Build Build'
            echo 'this is where i go into the stash some files to be used later here in Build Java 7 theoretical / Stash some files to be used later in the build'
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
        stage('Test A 7') {
          steps {
            echo 'echo I\'m glad it worked but hopefully this will test out and deploy'
            echo 'i would here have a node for build java 7 had i had the option under the node selection from cloud bees this way the build would be tested and run on this node'
          }
        }

        stage('Test A 8') {
          steps {
            sh 'echo it worked and this is from CLI but delayed for 5'
            echo 'i would here have a node for build java 8 had i had the option under the node selection from cloud bees this way the build would be tested and run on this node'
          }
        }

        stage('Test B 7') {
          steps {
            echo 'this is the restore section of previously stashed info from Build Java 7 theoretical where I move by using the equal sign in teh restore files previoulsy stashed step and then rename the versions appropriately'
          }
        }
        stage('Test B 8) {
         steps {
           echo 'This would be the secondary version of the java 8 build test that I am literally coding currently and would develop seperately and this would probably be some other file type and execution code'
          }
        }
      }
    }

    stage('Deploy') {
      steps {
        echo 'echo How cool is it that I can do all of this and deploy it in this CLI but I understand the ui is valuable to test and see its success prior to this theoretical deployment'
        echo 'I showed mom what I am doing!!'
      }
    }

  }
}
