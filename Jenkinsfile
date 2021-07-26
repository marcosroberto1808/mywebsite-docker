pipeline {
    agent any

    stages {
        
        stage('Build') {
            steps {
                git 'https://github.com/marcosroberto1808/mywebsite-docker.git'
            }
        }
        
        stage('Ansible Ping') {
            steps {
                ansiblePlaybook disableHostKeyChecking: true, playbook: 'deploy-docker.yml'
            }
        }
        
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t mywebsite-docker-image .''
            }
        }
        
        stage('Run Docker Container') {
            steps {
                sh 'docker run --name mywebsite-docker-container -p 80:80 -d mywebsite-docker-image''
            }
        }
        
    }
}

