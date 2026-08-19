pipeline {
    agent any

    tools {
        maven 'Maven 3.8.6'
    }

    stages {
        stage('Checkout Code') {
            steps {
                echo 'Checking out code from GitHub...'
                git branch: 'main', url: 'https://github.com/RajaGopal-devops/java-devops-cicd-demo.git'
            }
        }

        stage('Build & Test') {
            steps {
                echo 'Building Java Application with Maven...'
                sh 'mvn clean package'
            }
        }

        stage('Build Docker Image') {
            steps {
                echo 'Building Docker Container Image...'
                sh 'docker build -t rajagopal/java-devops-demo:latest .'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application container...'
                sh 'docker run -d -p 8080:8080 rajagopal/java-devops-demo:latest'
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed.'
        }
        success {
            echo 'CI/CD Pipeline Succeeded!'
        }
        failure {
            echo 'CI/CD Pipeline Failed!'
        }
    }
}
