pipeline {
    agent any
    stages {

        stage('Deploy - Staging') {
            steps {
                bat 'deploy staging'
                bat 'run-smoke-tests'
            }
        }

        stage('Sanity check') {
            steps {
                input "Does the staging environment look ok?"
            }
        }

        stage('Deploy - Production') {
            steps {
                bat 'deploy production'
            }
        }
    }
}
