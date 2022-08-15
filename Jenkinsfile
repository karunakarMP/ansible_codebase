pipeline {
    agent any

    stages {
        stage('Validate lint') {
            steps {
                sh "ansible-lint"
            }
        }

        stage('Download Dependencies') {
            steps {
                sh "ansible-galaxy install -g -f -r roles/requirements"
            }
        }
    }

}


