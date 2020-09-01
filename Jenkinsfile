pipeline {
    agent {  label 'worker-aws-dynamic' }
    stages {
        stage('Build') { 
             steps {
                sh 'mvn clean package'
        }
        }
        stage('SonarQube analysis') { 
             steps {
                withSonarQubeEnv('sonar-way') { 
                sh 'mvn sonar:sonar'
                }
        }
        }
       
        
     }
        
    }
    }
