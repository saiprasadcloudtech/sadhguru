pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building a .Net App'
          }
        }

        stage('Test') {
          steps {
            echo 'Testing the application'
          }
        }

        stage('Test Log') {
          steps {
            writeFile(file: 'LogTestFile.txt', text: 'This is automated file log')
          }
        }

      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy') {
          steps {
            input(message: 'Do you still want to continue to deploy??', id: 'OK')
            echo 'Deploying the app in the IIS server'
          }
        }

        stage('Artifact') {
          steps {
            archiveArtifacts 'LogTextFile.txt'
          }
        }

      }
    }

  }
}