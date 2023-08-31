pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        git(url: 'https://github.com/matthewzabikhullaev/docker.git', branch: 'main')
      }
    }

  }
}