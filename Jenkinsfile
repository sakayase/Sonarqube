pipeline {
  agent any
  tools {
    maven 'Maven 3.9.9'
  }
  stages {
    stage ('Checkout') {
      steps {
        git 'https://github.com/ScaleSec/vulnado'
      }
    }
    stage ('Build') {
      steps {
        sh 'nvm clean package'
      }
    }
  }
}
