pipeline {
    agent any
    stages {
        stage('Installing Docker on Jenkins server'){
            steps {
              sh 'sudo dnf update -y'
              sh 'dnf clean all'
              sh 'sudo dnf config-manager --add-repo=https://download.docker.com/linux/centos/docker-ce.repo'
              sh 'sudo dnf install docker-ce --nobest -y'
              sh ' sudo systemctl start docker'
              sh 'sudo systemctl enable docker'
              sh 'sudo docker run hello-world'
              
           
            }
        }
        stage('Pulling docker image'){
          steps {
              sh 'sudo docker pull httpd'
          }
        }
    }
}
