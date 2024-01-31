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
                script {
                    // Define the path to the Ansible playbook and inventory
                    def playbookPath = "~/dev/playbk.yml"
                    def inventoryPath = "~/dev/inventory.yml"

                    // Run the Ansible playbook with the specified inventory
                    sh'pwd'
                    sh "ansible-playbook playbk.yml -l web"
                }
            }
        }
    }
}
