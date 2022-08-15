pipeline {
    agent any

    stages {

        stage('Download Dependencies') {
            steps {
                sh "ansible-galaxy install -r roles/requirements.yml -p roles/"
            }
        }

        stage('Validate lint') {
            steps {
                sh "ansible-lint"
            }
        }


    }

}


