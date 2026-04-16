pipeline {
    agent any

    environment {
        NETLIFY_SITE_ID = '53e09c9a-0419-488f-836a-b7f9cca9d32c'
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                echo "NETLIFY_SITE_ID: ${NETLIFY_SITE_ID}"
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
            publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, icon: '', keepAll: false, reportDir: '', reportFiles: 'index.html', reportName: 'HTML Report', reportTitles: '', useWrapperFileDirectly: true])
        }
    }


}
