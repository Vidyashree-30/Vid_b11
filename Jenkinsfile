pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                dir('code') {
                    git branch: 'dev', url: 'https://github.com/Vidyashree-30/Vid_b11.git'
                }
            }
        }

        stage('Unit Tests') {
            steps {
                dir('code') {
                    echo 'Running unit tests...'
                    sh 'mvn test'
                }
            }
        }
    }

    post {
        success {
            echo 'Tests ran successfully.'
        }
        failure {
            echo 'Tests failed.'
        }
    }
}
