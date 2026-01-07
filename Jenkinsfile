pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo "Building branch: ${env.BRANCH_NAME}"
                checkout scm
            }
        }

        stage('Run App') {
            steps {
                echo "Running the app..."
                sh 'node index.js'
            }
        }
    }

    post {
        success {
            echo "Pipeline for branch ${env.BRANCH_NAME} completed successfully!"
        }
    }
}

