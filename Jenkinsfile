pipeline {
    agent {
        docker {
            image 'node:24.11.0-alpine3.22'
            args '-v /jenkins:/workspace -w /workspace'
        }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --eval "console.log(process.arch,process.platform)"'
            }
        }
    }
}
