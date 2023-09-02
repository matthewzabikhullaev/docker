pipeline {
    agent any
    stages {
        stage('Install docker'){
            steps {
                sh 'sudo apt-get update -y && sudo apt-get install ca-certificates curl gnupg -y'
                sh 'sudo install -m 0755 -d /etc/apt/keyrings -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg ; sudo chmod a+r /etc/apt/keyrings/docker.gpg'
                sh 'echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null'
                sh 'sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y'
                sh 'sudo systemctl enable docker --now'
            }
        }
    }
}
