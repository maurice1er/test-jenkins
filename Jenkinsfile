pipeline {
    agent any
    environment {
        imageName = '70077007/test-jenkins'
        registryCredential = 'dockerhub-access'
        // '70077007/flask-neo4j'
        dockerImage = ''
    }

    stages {
        stage("Docker build"){
            sh 'docker version'
            sh 'docker tag mynginx:1.0.0 70077007/test-jenkins:0.0.1'
            // sh 'docker build -t jhooq-docker-demo .'
            // sh 'docker image list'
            /// sh 'docker tag jhooq-docker-demo rahulwagh17/jhooq-docker-demo:jhooq-docker-demo'
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
