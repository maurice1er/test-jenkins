pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker --version'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'ls -la'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
