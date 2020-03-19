pipeline { 
    agent any  
    stages { 
        stage('Build') { 
            steps { 
              // echo 'This is a minimal pipeline.'
                sh 'mvn clean install'
            }
        }
    }
}
