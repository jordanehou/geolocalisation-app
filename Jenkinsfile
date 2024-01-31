pipeline {
    agent any

    stages {
        stage('checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/jordanehou/geo-july.git'
            }
        }
        stage('Run Ansible Playbook') {
            steps {
                // Run the Ansible playbook
                sh 'ansible-playbook -i inventory_file playbook.yml'
            }
        }
    }
}
