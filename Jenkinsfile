pipeline {
    agent {
        docker {
            image '<your-docker-repo>/custom-node:16'
        }
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/KgMyatT/node-js-sample.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
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
