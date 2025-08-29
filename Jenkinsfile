pipeline {
    agent any

    tools {
        nodejs 'Node 24' // This should match your Jenkins tool setup
    }

    stages {
        stage('Checkout') {
            steps {
                    checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }
    }

    post {
        success {
            echo '🎉 Tests passed!'
        }
        failure {
            echo '❌ Tests failed!'
        }
    }
}
