pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from a Git repository
                git 'https://github.com/your/repository.git'
            }
        }
        stage('Build') {
            steps {
                // Execute the build steps here
                sh 'mvn clean install' // Example Maven build command
            }
        }
        stage('Deploy') {
            steps {
                // Deploy the built application
                sh 'ssh user@server "deploy-script.sh"' // Example deployment script execution
            }
        }
    }
}
