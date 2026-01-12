pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('CI Check') {
            steps {
                sh 'echo "CI pipeline running successfully"'
            }
        }
    }
}
