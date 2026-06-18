pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code...'
                checkout scm
            }
        }

        stage('List Files') {
            steps {
                echo 'Listing repo files'
                sh 'ls -l'
            }
        }

        stage('Read Files') {
            steps {
                echo 'Reading text files'
                sh 'cat file1.txt'
                sh 'cat file2.txt'
                sh 'cat file3.txt'
            }
        }
    }

    post {
        success {
            echo 'Build successful 🎉'
        }
        failure {
            echo 'Build failed ❌'
        }
    }
}
