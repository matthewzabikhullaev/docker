pipeline {
    agent any
    stages {
        stage('Installing Docker on Jenkins server'){
            steps {
              sh '''
              sudo dnf update -y
              sudo dnf config-manager --add-repo=https://download.docker.com/linux/centos/docker-ce.repo
              sudo dnf install docker-ce --nobest -y
              sudo systemctl start docker
              sudo systemctl enable docker
              sudo docker run hello-world
              '''
            }
        }
        
    }
}
