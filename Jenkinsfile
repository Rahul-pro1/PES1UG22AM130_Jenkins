pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ main.cpp -o output_PES1UG22AM130'
            }
        }

        stage('Test') {
            steps {
                sh './output_PES1UG22AM130'
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
