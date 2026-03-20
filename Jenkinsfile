pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Lint') {
            steps {
                echo 'Checking HTML syntax...'
                // This is a simple mock lint check
                sh 'grep -q "<html>" index.html || echo "Warning: Missing html tag"'
            }
        }
        stage('Archive') {
            steps {
                echo 'Archiving artifacts...'
                archiveArtifacts artifacts: 'index.html', fingerprint: true
            }
        }
    }
}