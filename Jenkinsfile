node() {
    stage('Build') {
        docker.image('node:lts-bullseye-slim').inside {
            sh 'node --version'
        }
    }
}