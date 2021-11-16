pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'pwd'
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
