pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building Java application'
                sh 'mvn -B clean package -DskipTests'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Maven tests'
                sh 'mvn -B test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Checking Ansible installation'
                sh 'ansible --version'
                sh 'ansible-playbook --version'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully'
        }
        failure {
            echo 'Pipeline failed. Check Console Output.'
        }
    }
}
