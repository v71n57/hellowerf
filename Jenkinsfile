node { 
    stage('Build') { 
        echo 'make' 
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