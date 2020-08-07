
pipeline {
  
    agent any
  
    stages {
      
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'mvnw clean package'
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
