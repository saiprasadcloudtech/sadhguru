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

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying the app in the IIS server'
      }
    }

  }
}