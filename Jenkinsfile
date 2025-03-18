pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ main.cpp -o PES1UG22AM130-1'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG22AM130-1'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment stage executed.'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline execution failed.'
        }
    }
}
