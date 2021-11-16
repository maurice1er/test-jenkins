pipeline {
    agent {
        label 'docker'
    }

    stages {
        stage('Build Image') {
            agent {
                docker {
                    label 'docker'
                    image '70077007/test-jenkins'
                }
            }
            steps {
                script {
                	// app = docker.build("70077007/test-jenkins")
                    sh '70077007/test-jenkins --version'
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
