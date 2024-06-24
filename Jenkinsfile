node {
    try {
        stage('Build') {
            echo 'Building...'
            // Add your build steps here, e.g.,
            // sh 'mvn clean install'
        }
        stage('Test') {
            echo 'Testing...'
            // Add your test steps here, e.g.,
            // sh 'mvn test'
        }
        stage('Deploy') {
            echo 'Deploying...'
            // Add your deploy steps here, e.g.,
            // sh 'scp target/myapp.war user@server:/path/to/deploy'
        }
    } catch (Exception e) {
        currentBuild.result = 'FAILURE'
        throw e
    } finally {
        if (currentBuild.result == 'FAILURE') {
            echo 'Pipeline failed.'
        } else {
            echo 'Pipeline succeeded.'
        }
        echo 'Pipeline completed.'
    }
}
