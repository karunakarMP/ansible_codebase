pipeline {
    agent any

    stages {
        stage('validate') {
            steps {
                sh "ansible-lint"
            }
        }
    }

}


