pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('checkout & build') {
            steps {
                checkout scm
            }
            steps {
                sh 'mvn package'
            }
        }
    }
}
