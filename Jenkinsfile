pipeline {
    agent none
    stages {
        
        stage('Back-end') {
            agent {
                label 'for-sequential'
            }
            
            steps {
                agent {
                docker { image 'maven:3-alpine' }
            }
                sh 'mvn --version'
            }
        }
        
    }
}
