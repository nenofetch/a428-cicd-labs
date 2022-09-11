node("react-app") {
    docker.build("node:lts-bullseye-slim").inside {
        stage('Build') {
            sh 'npm i'
        }
        stage('Test') {
            sh './jenkins/scripts/test.sh'
        }
    }
}