pipeline {
    agent any
    stages {
        stage('Build') { 
            
            steps {
             
                sh 'mvn clean package'
            }
        
        }
        stage('deploy') { 
            steps {
             
                sh 'echo deploy'
            }
       
        }
    }
}
