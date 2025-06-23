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

        stage('Build') {
            steps {
                dir('code') {
                    echo 'Building the project on dev branch...'
                    sh 'mvn clean install'
                }
            }
        }

        stage('Unit Tests') {
            steps {
                dir('code') {
                    echo 'Running unit tests on dev branch...'
                    sh 'mvn test'
                }
            }
        }

        stage('Package') {
            steps {
                dir('code') {
                    echo 'Packaging the build on dev branch...'
                    sh 'mvn package'
                }
            }
        }
    }

    post {
        success {
            echo 'Dev branch build completed successfully.'
        }
        failure {
            echo 'Dev branch build failed.'
        }
    }
}
