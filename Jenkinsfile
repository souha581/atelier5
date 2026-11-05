pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                
                git branch: 'main', url: 'https://github.com/souha581/atelier5.git'
            }
        }

        stage('Build') {
            steps {
                
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                
                sh 'npm test'
            }
        }

        stage('Archive') {
            steps {
                
                archiveArtifacts artifacts: '**/dist/*.zip', allowEmptyArchive: true
            }
        }
    }
}
