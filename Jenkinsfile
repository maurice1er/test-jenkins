pipeline {
    agent any

    stages {
        stage('Build Dockerfile') {
            steps {
                sh 'pwd'
                sh 'ls -la'
                sh 'docker build -t mynginx:1.0.0  .'
            }
        }
        stage('Push to Dockerhub') {
            steps {
                sh 'docker tag mynginx:1.0.0 70077007/test-jenkins:0.0.1'
                sh 'docker push 70077007/test-jenkins:0.0.1'
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
