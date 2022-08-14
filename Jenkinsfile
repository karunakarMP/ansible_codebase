pipeline {
    agent any

    stages {
        stage('Validate lint') {
            steps {
                sh "ansible-lint"
            }
        }
    }

}


