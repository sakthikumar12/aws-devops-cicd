
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Jenkins has checked out the GitHub repository.'
            }
        }

        stage('Validate Files') {
            steps {
                sh 'test -f Dockerfile'
                sh 'test -f app/index.html'
                echo 'Application files verified successfully!'
            }
        }
    }

    post {
        success {
            echo 'CI pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the console output.'
        }
    }
}
