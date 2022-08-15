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
                sh "ansible-playbook playbook.yml"
            }
        }

        stage('Delete Slave Node') {
            steps {
                echo "Slave node deleted"
            }
        }


    }

}


