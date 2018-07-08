pipeline {
    
agent { label 'docker' }
    
    
  
    stages {
        
        stage('Clone sources') {
        git url: 'https://github.com/honeysundar/java_application.git'
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
