node() {
    def myDocker = docker.image('node:lts-alpine')

    myDocker.inside('-p 3000:3000') {
        checkout
        
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