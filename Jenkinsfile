pipeline {
    agent any

    stages {

        stage('1. Checkout Code') {
            steps {
                git url: 'YOUR_REPO_URL'
            }
        }

        stage('2. Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('3. Build') {
            steps {
                sh 'npm run build || echo "No build step"'
            }
        }

        stage('4. Unit Tests') {
            steps {
                sh 'npm test || true'
            }
        }

        stage('5. Code Quality (SonarCloud)') {
            steps {
                echo 'SonarCloud analysis step here'
            }
        }

        stage('6. Security Scan') {
            steps {
                sh 'npm audit || true'
            }
        }

        stage('7. Package') {
            steps {
                sh 'npm pack'
            }
        }

    }
}
