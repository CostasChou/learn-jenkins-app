pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps{
                sh '''
                    node --version
                    npm --version
                    ls -la
                    npc -ci
                    npm run build 
                '''        
            }
        }
    }
}
