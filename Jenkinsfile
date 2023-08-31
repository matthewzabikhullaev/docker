pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/matthewzabikhullaev/docker.git', branch: 'main')
      }
    }

    stage('Sleep') {
      steps {
        sleep 5
      }
    }

    stage('change dir') {
      steps {
        dir(path: '/home/')
      }
    }

  }
}