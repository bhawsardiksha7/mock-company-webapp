pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh './gradlew assemble'  // Build command
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh './gradlew test'  // Test command
            }
        }
    }

    post {
        success {
            echo 'Build and tests passed!'
        }
        failure {
            echo 'Build or tests failed!'
        }
    }
}
