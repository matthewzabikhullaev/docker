pipeline {
  agent any
  stages {
    stage('Checkout code') {
      steps {
        echo 'Building'
        git(url: 'https://github.com/matthewzabikhullaev/docker.git', branch: 'main')
      }
    }

    stage('Test') {
      steps {
        sh 'echo "Hello World"'
      }
    }

  }
}