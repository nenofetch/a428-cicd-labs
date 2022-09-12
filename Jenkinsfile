node() {
    stage('Build') {
        docker.image('node:lts-bullseye-slim').inside {
            sh 'npm i'
        }
    }
    stage('Test') {
        sh './jenkins/scripts/test.sh'
    }
}