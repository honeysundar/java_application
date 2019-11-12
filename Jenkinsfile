pipeline {
    agent {
        label 'slave'
    }
    stages {
        agent {
        label 'slave'
    }
        stage('Back-end') {
            agent {
                docker { image 'maven:3-alpine' }
            }
            
            steps {
                sh 'mvn --version'
            }
        }
        
    }
}
