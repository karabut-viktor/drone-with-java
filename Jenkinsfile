pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building..'
      }
    }
    stage('Test') {
      parallel {
        stage('Unit') {
          steps {
            echo 'Running unit tests'
          }
        }
        stage('Integration') {
          steps {
            echo 'Running integration tests'
          }
        }
        stage('Ent2End') {
          steps {
            echo 'Running End2End tests'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }
  }
}