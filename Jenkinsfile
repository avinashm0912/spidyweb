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
            junit 'testing-results/junit.xml'
        }
    }


}
