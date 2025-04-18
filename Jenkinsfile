pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/your-username/java-docker.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("java-hello")
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker run --rm java-hello'
            }
        }
    }
}
