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
                    def playbookPath = "/home/ec2-user/dev/playbk.yml"
                    def inventoryPath = "/home/ec2-user/dev/inventory.yml"

                    // Run the Ansible playbook with the specified inventory
                    sh "ansible-playbook ${playbookPath} -l web"
                }
            }
        }
    }
}
