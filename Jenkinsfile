pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t jenkins-flask-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh '''
                docker stop jenkins-app || true
                docker rm jenkins-app || true
                docker run -d -p 5000:5000 --name jenkins-app jenkins-flask-app
                '''
            }
        }
    }
}

