pipeline {
    agent {
        node {
            label 'docker'
        }
    }

    stages {
        stage('Build Image') {
            steps {
                script {
                	app = docker.build("70077007/test-jenkins")
                }
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
