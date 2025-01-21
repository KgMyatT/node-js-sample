pipeline {
    agent {
        docker { image 'node:16' }  // Use official Node.js Docker image
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/KgMyatT/node-js-sample.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'  // This will run inside the container with Node.js and npm
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
                // Deployment commands here
            }
        }
    }
}
