pipeline {
    agent any
    stages {
        stage('Back-end') {
            agent {
                slave { image 'maven:3-alpine' }
            }
            
            steps {
                sh 'mvn --version'
            }
        }
        
    }
}
