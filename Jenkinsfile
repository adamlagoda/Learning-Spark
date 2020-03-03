pipeline {
    agent { docker { image 'maven:3.3.3'} }
    stages {
        stage('build') {
            steps {
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
            echo 'This will always run'
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