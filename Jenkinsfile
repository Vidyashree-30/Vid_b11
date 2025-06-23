pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'mvn clean install'
            }
        }
    }

    post {
        success {
            echo 'Build completed successfully.'
        }

        failure {
            echo 'Build failed.'
        }

        unstable {
            echo 'Build is unstable (e.g. test failures).'
        }

        aborted {
            echo 'Build was aborted.'
        }

        always {
            echo 'This runs after every build result.'
        }
    }
}
