node {
    stage('Build') {
        sh 'sudo apt-get install gmake cmake git && curl -L https://bit.ly/n-install | bash -s -- -y lts && npm i'
    }
    stage('Test') {
        echo 'Testing...'
    }
    stage('Deploy') {
        echo 'Deploying...'
    }
}