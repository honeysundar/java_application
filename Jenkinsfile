pipeline {
    
agent { label 'docker' }
    
    
  
    stages {
        
        stage('Checkout') {
        checkout scm
    }
        stage('Build') {
            steps {
                echo 'Building..'
                 sh 'mvn package'
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
