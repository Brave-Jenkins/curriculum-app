pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/Brave-Jenkins/curriculum-app', branch: 'dev')
      }
    }

    stage('Logs') {
      steps {
        sh 'ls -la'
      }
    }

    stage('Build') {
      steps {
        sh 'docker build -f curriculum-front/Dockerfile .'
      }
    }

  }
}