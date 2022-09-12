node() {
    docker.image('node:lts-bullseye-slim').inside {
        stage('Build') {
            
                git branch: 'react-app', url: '/home/Documents/Belajar_Implementasi_CICD/Jenkins/a428-cicd-labs'
                sh 'npm i'
        }
    
        stage('Test') {
            git branch: 'react-app', url: '/home/Documents/Belajar_Implementasi_CICD/Jenkins/a428-cicd-labs'
            sh './jenkins/scripts/test.sh'
        }
    } 
}