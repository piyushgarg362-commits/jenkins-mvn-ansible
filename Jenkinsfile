pipeline {
    agent any

    stages {
        stage('Check Jenkins') {
            steps {
                echo 'Jenkins pipeline is working!'
            }
        }

        stage('Check Java') {
            steps {
                sh 'java -version'
            }
        }

        stage('Check Ansible') {
            steps {
                sh 'ansible --version'
            }
        }
    }
}
