pipeline {
    agent {
        docker-slave {
            image 'maven:3-alpine'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
