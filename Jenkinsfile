pipeline {
    agent any
    
    parameters {
        booleanParam(name: 'executeTests', defaultValue: true)
    }
    
    environment {
        VERSION = '1.0.0'
    }
    
    tools {
        maven 'Maven'
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo "Version: ${VERSION}"
                bat 'mvn -version'
            }
        }
        stage('Test') {
            when {
                expression { params.executeTests == true }
            }
            steps {
                echo 'Testing with conditions..'
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
