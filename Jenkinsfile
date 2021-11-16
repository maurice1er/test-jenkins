pipeline {
    /* agent {
        label 'docker'
    } */

    stages {

	stage('Build and Run docker image') {
             steps {
                sh "docker build -t 70077007/test-jenkins:1.0.${BUILD_NUMBER} ."
                script {
                    try {
                        sh 'docker rm -f 70077007/test-jenkins'
                    }catch (exc) {
                        echo 'Erreur de suppression'
                    }
                }
                sh "docker run --name 70077007/test-jenkins:1.0.${BUILD_NUMBER} -d -p 8008:5000 70077007/test-jenkins:1.0.${BUILD_NUMBER}"
            }
         }     

	    
	    
        /* stage('Build Image') {
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
        } */ 
    }
}
