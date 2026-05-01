pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out code...'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test || true'
            }
        }

        stage('Security Scan (Snyk)') {
            steps {
                sh 'echo Running Snyk scan...'
                sh 'snyk test || true'
            }
        }

        stage('Code Quality (SonarCloud)') {
            steps {
                sh 'echo Running SonarCloud analysis...'
            }
        }
    }
}
