pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning repository...'
                checkout scm
            }
        }
        stage('Hello') {
            steps {
                echo 'Pipeline is working!'
                sh 'whoami'
                sh 'date'
            }
        }
    }

    post {
        success {
            echo 'Build succeeded!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
