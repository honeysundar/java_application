pipeline {
    agent any

    stages {
        stage('Build') {
                agent {
                        docker { image 'maven:3-alpine' }
                      }
            steps {
                sh 'mvn package'
                  }
                      }
        
        stage('Docker image to created') {
            steps {
                sh 'docker build -t java_app .'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
