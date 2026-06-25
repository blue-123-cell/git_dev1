pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/blue-123-cell/git_dev1.git'
            }
        }
        stage('Test') {
            steps {
                bat 'docker build -t web-image-app .'
            }
        }
        stage('Run Docker Container') {
            steps {
                bat 'docker run -d -p 8090:80  web-image-app'
            }
        }
    }
}