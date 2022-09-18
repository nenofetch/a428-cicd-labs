node() {
    

        stage('Build') {
            docker.image('node:lts-alpine').inside {
                git branch: 'react-app', url: '/home/Documents/Belajar_Implementasi_CICD/Jenkins/a428-cicd-labs'
                sh 'npm i'
            }
        }
    
        stage('Test') {
            docker.image('node:lts-alpine').inside {
                git branch: 'react-app', url: '/home/Documents/Belajar_Implementasi_CICD/Jenkins/a428-cicd-labs'
                sh './jenkins/scripts/test.sh'
                input message: 'Lanjut tahap Deploy? (Klik "Proceed" untuk melanjutkan ke tahap deploy)'
            }
        }
        stage('Deploy') {
            docker.image('node:lts-alpine').inside {
                git branch: 'react-app', url: '/home/Documents/Belajar_Implementasi_CICD/Jenkins/a428-cicd-labs'
                sh './jenkins/scripts/deliver.sh'
                input message: 'Sudah selesai menggunakan React App? (Klik "Proceed" untuk mengakhiri)'
                sleep time: 60, unit: 'SECONDS'
                sh './jenkins/scripts/kill.sh'            
            }
        }
    
}