node {
    agent any
    stage('Build') {
        // installing npm i
        sh 'npm i'
    }
    stage('Test') {
        // running npm test
        sh './jenkins/scripts/test.sh'
    }
}