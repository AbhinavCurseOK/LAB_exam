pipeline {
    agent any

    environment {
        DOCKER_IMAGE = 'hellomam'  // Use 'hellomam' as the Docker image name
    }

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    echo 'Building Docker Image...'
                    // Build the Docker image using the Dockerfile
                    sh 'docker build -t $DOCKER_IMAGE .'
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    echo 'Running Docker Container...'
                    // Run the Docker container
                    sh 'docker run $DOCKER_IMAGE'
                }
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished'
        }
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
