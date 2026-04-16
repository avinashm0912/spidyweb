pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
    post {
       always {
            // This will no longer fail the build when no tests exist
            junit (
                allowEmptyResults: true,
                testResults: 'testing-results/junit.xml'
            )
        }
    }


}
