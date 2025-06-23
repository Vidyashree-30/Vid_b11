pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                dir('code') {
                    git branch: 'dev', url: 'https://github.com/Vidyashree-30/Amazon-Jenkins.git'
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
