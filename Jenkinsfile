pipeline {
    agent any

    stages {

        stage('Fetch Requirements') {
            steps {
                sh "ansible-galaxy install -r roles/requirements.yml"
            }
        }

        stage('Validate lint') {
            steps {
                sh "ansible-lint"
            }
        }

        stage('Create Slave Node') {
            steps {
                echo "Slave node Created"
            }
        }


    }

}


