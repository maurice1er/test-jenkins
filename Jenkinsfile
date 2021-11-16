pipeline {
    agent any
    environment {
        imageName = '70077007/flask-neo4j'
        registryCredential = 'dockerhub-access'
        // '70077007/flask-neo4j'
        dockerImage = ''
    }

    stages {
        stage('Build Docker image') {
            steps {
                script {
                    dockerImage = docker.build imageName
                }
                // sh 'docker build -t mynginx:1.0.0  .'
            }
        }
        /* stage('Push to Dockerhub') {
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
        } */
    }
}
