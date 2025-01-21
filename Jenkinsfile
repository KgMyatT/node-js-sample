pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/KgMyatT/node-js-sample.git'
            }
        }
        stage('Install Node.js and npm') {
            steps {
                sh '''
                # Install Node.js and npm
                apt-get update
                apt-get install -y nodejs npm
                npm install
                '''
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }
}
