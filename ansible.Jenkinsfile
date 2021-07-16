pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                
                git branch: 'main', url: 'https://github.com/vytec-app/ansible.git'

                ansiblePlaybook installation: 'ansible', inventory: 'inventory.yml', playbook: 'nginx.yml'
           
            }
        }
    }
}

