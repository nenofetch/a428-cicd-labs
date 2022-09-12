node() {
//     dir('/home/Documents/Belajar_Implementasi_CICD/Jenkins/a428-cicd-labs') {
//     stage('Build') {
//         docker.image('node:lts-bullseye-slim').inside {
//             sh 'npm i'
//         }
//     }
//     stage('Test') {
//         sh './jenkins/scripts/test.sh'
//     }
// }
    stage('Test') {
        docker.image('node:lts-bullseye-slim').inside {
            sh 'ls /home'
        }
    }

 
}