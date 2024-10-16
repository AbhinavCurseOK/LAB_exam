pipeline {
    agent {
        docker {
            image 'python:3.9'
        }
    }

    stages {
        stage('Run Python Script') {
            steps {
                sh 'python hello.py'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished'
        }
    }
}
