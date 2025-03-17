pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building project...'
                    sh 'g++ main.cpp -o YOUR_SRN-1'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    echo 'Testing project...'
                    sh './output'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying project...'
                    sh 'echo Deployment successful!'
                }
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
