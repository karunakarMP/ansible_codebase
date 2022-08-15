pipeline {
    agent any

    stages {

        stage('Download Dependencies') {
            steps {
                sh "ansible-galaxy install -g -f -r roles/requirements"
            }
        }

        stage('Validate lint') {
            steps {
                sh "ansible-lint"
            }
        }


    }

}


