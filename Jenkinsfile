pipeline {
    agent any
   
    stages {

        stage('pull') {
            steps {
                git branch: 'main', url: 'https://github.com/vidyashree-30/Amazon-Jenkins.git'
            }
        }

        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }

    post {
        always {
            echo 'This runs after every build result.'
        }
    }
}
