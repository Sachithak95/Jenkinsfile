pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Starting the Build stage...'
               
                echo 'Build completed successfully.'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Starting the Unit and Integration Tests stage...'
               
                echo 'Unit and Integration Tests completed successfully.'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Starting the Code Analysis stage...'
               
                echo 'Code Analysis completed successfully.'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Starting the Security Scan stage...'
                echo 'Security Scan completed successfully.'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Starting the Deploy to Staging stage...'
            
                echo 'Deployment to Staging completed successfully.'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Starting the Integration Tests on Staging stage...'
               
                echo 'Integration Tests on Staging completed successfully.'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Starting the Deploy to Production stage...'
            
                echo 'Deployment to Production completed successfully.'
            }
        }
    }
    post {
        failure {

            emailext subject: 'Pipeline Failed',
                body: 'The Jenkins pipeline has failed. Please check the logs for details.',
                attachLog: true,
                to: 'dpmdj199@gmail.com'
        }
        success {
     
            emailext subject: 'Pipeline Succeeded',
                body: 'The Jenkins pipeline has succeeded.',
                attachLog: true,
                to: 'dpmdj199@gmail.com'
        }
    }
}