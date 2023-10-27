node {
    stage('Checkout') {
        git branch: 'main', url: 'https://github.com/Youmnaibrahim/simple-java-app.git'
    }

    stage('Build') {
        try {
            sh 'echo "Build stage"'
        } catch (Exception e) {
            sh 'echo "Exception found"'
            throw e
        }
    }

    stage('Test') {
        if (env.BRANCH_NAME == 'FEAT') {
            sh 'echo "Test stage"'
        } else {
            sh 'echo "Skip test stage"'
        }
    }
}
