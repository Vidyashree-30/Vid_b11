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
                bat 'mvn compile'
            }
        }

        stage('test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('build') {
            steps {
                bat 'mvn clean install'
            }
        }
    }

    post {
        always {
            echo 'This runs after every build result.'
        }
    }
}
