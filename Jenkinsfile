pipeline {
    agent any
    stages {
        stage('Build') { 
             steps {
                sh 'echo build'
                script {
              timeout(time: 10, unit: 'MINUTES') {
                input(id: "Deploy Gate", message: "Deploy ${params.project_name}?", ok: 'Deploy')
              }
            }
        }
            
        }
        stage('SonarQube analysis') { 
             steps {
                
                sh 'echo sonar'
              
        }
        }
        
        }
        
    }
