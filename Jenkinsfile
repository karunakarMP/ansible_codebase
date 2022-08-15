pipeline {
    agent any

    stages {

        stage('Fetch Requirements') {
            steps {
                sh "ansible-galaxy install -r requirements.yml"
            }
        }

        // stage('Validate lint') {
        //     steps {
        //         sh "ansible-lint"
        //     }
        // }

        stage('Create Slave Node') {
            steps {
                echo "Slave node Created"
            }
        }

        stage('Run Playbook') {
            steps {
                ansiblePlaybook credentialsId: 'ansible', disableHostKeyChecking: true, installation: 'Ansible2', playbook: 'playbook.yml'
            }
        }

        stage('Delete Slave Node') {
            steps {
                echo "Slave node deleted"
            }
        }


    }

}


