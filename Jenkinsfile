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
