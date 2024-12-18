pipeline {
    agent any

    stages {
        stage('Hello w/docker'){
            agent {
                docker {
                    image 'node:18-alpine'
                    //args '-u 1000:1000 --privileged'
                }
            }
            steps {
                sh '''
                    ls -la
                    node --version
                    npm --version
                    npm ci
                    npm run build
                    ls -la
                '''
            }
        }
    }
}
