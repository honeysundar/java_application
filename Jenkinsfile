pipeline {
    agent any
        stages {
        stage('Build') { 
            
        
            agent {
                docker { image 'lacosted/mavenjava' }
            }
            steps {
                sh 'mvn --version'
            }
        }
            
 
            
            
        
    }
}
