node() {
    def myDocker = docker.run('node:lts-alpine', '-p 3000:3000')
    
    
    myDocker.inside {
        checkout scm
        
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