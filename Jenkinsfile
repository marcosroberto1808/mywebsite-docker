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
    }
}

