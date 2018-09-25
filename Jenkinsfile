pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                checkout scm
                sh 'mvn package'
                stash includes: '**/target/*.war', name: 'grants'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
