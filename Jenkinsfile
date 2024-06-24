pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                echo 'Installing npm dependencies...'
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'npm run build'  // Adjust the command according to your project setup
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'  // You can add npm test if you have a test script in package.json
                // sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'  // Adjust the deploy command according to your setup
                // Example: sh 'npm run deploy'
            }
        }
    }

    post {
        always {
            echo 'Cleaning up...'
            // Optionally, clean up steps can be added here if needed
        }
        success {
            echo 'Pipeline succeeded.'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
