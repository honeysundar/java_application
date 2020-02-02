pipeline {
    agent any
    stages {
        stage('Build') { 
             
                sh 'mvn clean package'
        
        }
        stage('deploy') { 
             
                sh 'echo "deploy"'
       
        }
    }
}
