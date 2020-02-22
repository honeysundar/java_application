pipeline {
    agent docker {
        docker {
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
