node() {
    def myDocker = docker.image('node:lts-alpine')
    
    
    myDocker.inside {
        git branch: 'react-app', url: '/home/Documents/Belajar_Implementasi_CICD/Jenkins/a428-cicd-labs'
        
        stage('Build') {
                sh 'npm i'
        }
    
        stage('Test') {
            sh './jenkins/scripts/test.sh'
            input message: 'Lanjut tahap Deploy? (Klik "Proceed" untuk melanjutkan ke tahap deploy)'
        }

        stage('Deploy') {
            sh './jenkins/scripts/deliver.sh'
            input message: 'Sudah selesai menggunakan React App? (Klik "Proceed" untuk mengakhiri)'
            sleep time: 60, unit: 'SECONDS'
            sh './jenkins/scripts/kill.sh'      
        }
    }
}