node { 
    stage('Checkout') {
        checkout scm
    }
    stage('Build') { 
        sh 'werf converge --repo registry.example.com:5000/hleb' 
    }
    stage('Test') {
        echo 'make check'
    }
    if (currentBuild.currentResult == 'SUCCESS') {
        stage('Deploy') {
            echo 'make publish'
        }
    }
}
