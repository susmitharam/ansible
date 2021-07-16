pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                
                git branch: 'main', url: 'https://github.com/vytec-app/ansible.git'

                ansiblePlaybook credentialsId: 'root', installation: 'ansible', inventory: 'inventory.yml', playbook: 'nginx.yml'
           
            }
        }
    }
}

