
pipeline {
    agent any

    options {
        skipDefaultCheckout(true)
        timestamps()
    }

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code...'
                checkout scm
            }
        }

        stage('Verify') {
            steps {
                echo 'Verifying repository...'
                sh 'pwd'
                sh 'ls -la'
                sh 'git log -1 --oneline'
            }
        }

        stage('Build') {
            steps {
                echo 'Starting build...'
                sh 'echo "Build successful!"'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo "All tests passed!"'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Starting deployment...'
                sh 'echo "Deployment successful!"'
            }
        }
    }

    post {
        success {
            echo 'PIPELINE SUCCESS!'
        }

        failure {
            echo 'PIPELINE FAILED!'
        }

        always {
            echo 'Pipeline execution completed.'
        }
    }
}
