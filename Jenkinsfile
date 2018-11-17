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
        stage('build docker image'){
            agent any
            steps {
            sh 'docker build -t java_app .'
            }
        }
       
        stage('Push Docker image TO ECR'){
            agent any
            steps {
            
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
