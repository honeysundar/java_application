pipeline {
    agent { label 'docker' }
    stages {
        stage('Back-end') {
            agent {
                docker { image 'maven:3-alpine' }
            }
            steps {
                sh 'mvn package'
            }
        }
        
    }
}
