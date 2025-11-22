pipeline {
    agent any
    
    environment {
        VERSION = '1.0.0'
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo "Version: ${VERSION}"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying..'
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline Completed'
        }
    }
}
