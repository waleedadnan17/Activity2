pipeline {
    agent any

    stages {
        stage('Set up Python') {
            steps {
                // Use bat for Windows batch command
                bat 'python -m venv venv'
                bat 'venv\\Scripts\\activate'
            }
        }
        stage('Install dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }
        stage('Run tests') {
            steps {
                bat 'pytest'
            }
        }
    }
}
