pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ main.cpp -o PES2UG22CS131-1'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './PES2UG22CS131-1'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
