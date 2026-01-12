pipeline {
    agent any
    stages {
        stage('Checkout') { steps { checkout scm } }
        stage('Run') { steps { sh 'node -v && node server.js' } }
        stage('Archive') { steps { archiveArtifacts artifacts: '**/*', fingerprint: true } }
    }
}
