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
        sh 'curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash'
        sh 'nvm clean package'
      }
    }
  }
}
