pipeline {
    agent any 

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...in qa to test webhook'
                // Example for Node.js: sh 'npm install'
                // Example for Java: sh 'mvn clean package'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Running unit tests...'
                // Example: sh 'npm test'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying the application to qa...'
                // Example: sh './deploy.sh'
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution complete.'
        }
        success {
            echo 'The build was successful!'
        }
        failure {
            echo 'The build failed. Check the logs.'
        }
    }
}
