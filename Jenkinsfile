pipeline {
    agent {
        label '!windows'
    }
    environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE = 'sqlite'
    }
    stages {
        stage('Build') {
            steps {
                echo "Database engine is ${DB_ENGINE}"
                echo "DISABLE_AUTH is ${DISABLE_AUTH}"
                bat 'set'
            }
        }
        stage('Test') {
            steps {
                bat 'echo "Fai!" exit 1'
            }
        }
    }
    post {
        always {
            echo 'This will run always'
            }
        success {
            echo 'This will run on success'
            }
        failure {
            echo 'This will run on failure'
            }
        unstable {
            echo 'This will run only if run was marked as unstable'
            }
        changed {
            echo 'This will run only the state of pipeline changed'
            echo 'For wxample if, pipeline was previously failing but is now successful'
            }
    }
}