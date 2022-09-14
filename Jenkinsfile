node() {
    docker.image('node:lts-alpine').inside {
        git branch: 'react-app', url: '/home/Documents/Belajar_Implementasi_CICD/Jenkins/a428-cicd-labs'

        stage('Build') {
            sh 'npm i'
        }
    
        stage('Test') {
            sh './jenkins/scripts/test.sh'
        }
        stage('Deploy') {
            sh './jenkins/scripts/deliver.sh'
            input message: 'Sudah selesai menggunakan React App? (Klik "Proceed" untuk mengakhiri)'
            sh './jenkins/scripts/kill.sh'            
        }
    } 
}