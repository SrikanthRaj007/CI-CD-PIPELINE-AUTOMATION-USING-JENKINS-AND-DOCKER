pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'master',
                url: 'https://github.com/SrikanthRaj007/Jenkin_Automation_Docker.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t jenkins-flask-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh '''
                docker stop jenkins-flask || true
                docker rm jenkins-flask || true
                docker run -d -p 5000:5000 --name jenkins-flask jenkins-flask-app
                '''
            }
        }
    }
}
