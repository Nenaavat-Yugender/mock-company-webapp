pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh './gradlew assemble'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh './gradlew test'
            }
        }
    }

    post {
        success {
            echo 'Build and tests succeeded!'
        }
        failure {
            echo 'Build or tests failed!'
        }
    }
}

