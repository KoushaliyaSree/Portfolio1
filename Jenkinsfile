pipeline {
    agent any

       tools {
        // Define Node.js tool named 'NodeJS'
        nodejs 'node'
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from your version control system
                  git branch: 'main', url: 'https://github.com/KoushaliyaSree/Portfolio1.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                // Install Node.js dependencies using npm
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                // Build your React application
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                // Run tests for your React application
                echo "npm test"
            }
        }

      
    }

    post {
        success {
            // Send success notification (if needed)
            echo 'Build successful - Sending notification'
        }
        failure {
            // Send failure notification (if needed)
            echo 'Build failed - Sending notification'
        }
    }
}
