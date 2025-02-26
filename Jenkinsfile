pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/vaibhavvenkatM/my_python_project.git'
            }
        }

        stage('Build') {
            steps {
                sh 'python -m build --wheel'
            }
        }

        stage('Test') {
            steps {
                sh 'pytest tests/'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add deployment steps here if needed
            }
        }
    }
}
