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
                	app = docker.build("70077007/test-jenkins")
                    // sh '70077007/test-jenkins --version'
                }
            }
        }
        stage('Push Image') {
            steps {
                script {
			        docker.withRegistry('https://registry.hub.docker.com', 'dockerhub-access') {
			        	app.push("${BUILD_NUMBER}")
			            app.push("latest")
			        }
                }
            }
        }  
    }
}
