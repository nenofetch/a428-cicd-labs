node() {
    dir('/home/Documents/Belajar_Implementasi_CICD/Jenkins/a428-cicd-labs') {
    stage('Build') {
        docker.image('node:lts-bullseye-slim').inside {
            sh 'cd /home/Documents/npm i'
        }
    }
    stage('Test') {
        sh './jenkins/scripts/test.sh'
    }
}
 
}