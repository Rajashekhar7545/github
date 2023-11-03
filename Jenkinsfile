pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building the project"'
                // Add commands to build the project here
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Running tests"'
                // Add commands to run tests here
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying the project"'
                // Add commands to deploy the project here
            }
        }
    }
    post {
        always {
            sh 'echo "Cleanup"'
            // Add any cleanup commands here
        }
        success {
            sh 'echo "Project deployed successfully"'
            // Add any success message or commands here
        }
        failure {
            sh 'echo "Failed to deploy the project"'
            // Add any failure message or commands here
        }
    }
}
