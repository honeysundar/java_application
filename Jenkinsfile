pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('checkout & build') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
