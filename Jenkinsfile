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
        input(message: 'Do you still want to continue to deploy??', id: 'OK')
        echo 'Deploying the app in the IIS server'
      }
    }

  }
}