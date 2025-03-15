pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/RituKumari24/PES2UG22CS452_jenkins.git'
            }
        }

        stage('Build') {
            steps {
                sh 'g++ -o PES2UG22CS452-1 main.cpp'
            }
        }

        stage('Test') {
            steps {
                sh './PES2UG22CS452-1'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
