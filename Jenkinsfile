node('docker') {
    stage('Build') {
        docker.image('node:16.13.1-alpine').inside {
            sh 'node --version'
        }
    }
}