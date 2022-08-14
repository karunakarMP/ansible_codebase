pipeline {
    agent any

    stages {
        stage('validate') {
            steps {
                sh "ansible-lint sample_playbook.yml"
            }
        }
    }

}


