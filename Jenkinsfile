pipeline {
    agent {
        docker { image 'maven:3-alpine' }
        environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
    }
    }
    stages {
        stage('Test') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
