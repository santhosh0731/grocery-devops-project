pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git 'https://github.com/yourusername/grocery-devops-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t grocery-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8084:80 grocery-app || true'
            }
        }
    }
}
