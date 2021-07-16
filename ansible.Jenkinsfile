pipeline {
    agent any

    tools {
        tool name: 'ansible', type: 'org.jenkinsci.plugins.ansible.AnsibleInstallation'
    }

    stages {
        stage('Build') {
            steps {
                
                git 'https://github.com/vytec-app/ansible.git'

                ansiblePlaybook installation: 'ansible', inventory: 'inventory.yml', playbook: 'nginx.yml'
           
            }
        }
    }
}

