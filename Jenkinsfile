pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build the project'
      }
    }
    stage('Upload to registry') {
      steps {
        echo 'Upload to registry'
      }
    }
    stage('Pull on server') {
      steps {
        echo 'Pull image on the server'
      }
    }
    stage('Start the app') {
      steps {
        echo 'Restart docker-compose to use the new image'
      }
    }
  }
}