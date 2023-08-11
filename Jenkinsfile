pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/Brave-Jenkins/curriculum-app', branch: 'dev')
      }
    }

    stage('Logs') {
      parallel {
        stage('Logs') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Front-End Unit tests') {
          steps {
            sh 'cd curriculum-front && npm i && run test:unit'
          }
        }

      }
    }

  }
}