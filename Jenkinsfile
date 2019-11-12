pipeline {
    agent none
    stages {
        
        stage('Back-end') {
            
            steps {
                agent {
                docker { image 'maven:3-alpine' }
            }
                sh 'mvn --version'
            }
        }
        
    }
}
