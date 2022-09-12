node() {
    docker.image('node:lts-alpine').inside {
        git branch: 'react-app', url: '/home/Documents/Belajar_Implementasi_CICD/Jenkins/a428-cicd-labs'

        stage('Build') {
            sh 'npm i'
        }
    
        stage('Test') {
            sh './jenkins/scripts/test.sh'
        }
    } 
}