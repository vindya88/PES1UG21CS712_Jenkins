pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS712-1'
                sh 'g++ hello.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
