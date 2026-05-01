stage('Build') {
    steps {
        echo 'Building project...'
    }
}

stage('Unit Tests') {
    steps {
        sh 'npm test'
    }
}

stage('Code Analysis') {
    steps {
        echo 'Running SonarCloud...'
    }
}

stage('Security Scan') {
    steps {
        sh 'snyk test'
    }
}

stage('Deploy to Staging') {
    steps {
        echo 'Deploying to staging...'
    }
}

stage('Integration Tests') {
    steps {
        echo 'Running integration tests...'
    }
}

stage('Deploy to Production') {
    steps {
        echo 'Deploy complete'
    }
}
