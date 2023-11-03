pipeline {
    agent any
    environment {
        appDir = 'my_web_app'
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/yourusername/my_web_app.git'
            }
        }
        stage('Build') {
            steps {
                script {
                    sh "cd ${appDir} && npm install"
                    sh "cd ${appDir} && npm run build"
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh "cd ${appDir} && npm run test"
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh "cp -r ${appDir}/build /var/www/html"
                }
            }
        }
    }
    post {
        always {
            cleanWs()
        }
        success {
            echo 'Deployment successful!'
        }
        failure {
            echo 'Deployment failed!'
        }
    }
}
