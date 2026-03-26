pipeline {
    agent any

    stages {
        stage('Build Image') {
            steps {
                sh 'docker build -t devops-frontend ./frontend'
            }
        }

        stage('Build Frontend') {
            steps {
                sh 'docker run --rm devops-frontend npm run build'
            }
        }
    }
}