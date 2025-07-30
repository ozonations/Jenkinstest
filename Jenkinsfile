pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Cloning repository...'
                // Jika kamu pakai GitHub, bisa pakai:
                git url: 'https://github.com/ozonations/Jenkinstest.git'
                sh 'ls -la'
            }
        }

        stage('Build') {
            steps {
                echo 'Build step...'
                // Misalnya compile atau build
                sh './app.sh'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing step...'
                // Contoh test dummy
                sh 'echo "All tests passed."'
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded.'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
