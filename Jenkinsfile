pipeline {
    agent any

    stages {
        stage('Build Image') {
            steps {
                sh 'docker build -t devops-compose-app .'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'docker run --rm devops-compose-app npm test'
            }
        }
    }
}