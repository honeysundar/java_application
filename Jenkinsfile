pipeline {
    agent {  label 'worker-aws-dynamic' }
    stages {
        stage('Build') { 
             steps {
                sh 'mvn clean package'
        }
        }
       
        
     }
        
    }
