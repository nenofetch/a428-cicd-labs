node {
    env.NODEJS_VERSION = '16.13.0'

    stage('Build') {
        sh 'curl -L https://bit.ly/n-install | bash -s -- -y lts && npm i'
    }
    stage('Test') {
        echo 'Testing...'
    }
    stage('Deploy') {
        echo 'Deploying...'
    }
}