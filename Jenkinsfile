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
                def customImage = docker.build("maven:3-alpine")

    customImage.inside {
        sh 'mvn package'
        sh 'docker build -t java_app .'
                         }
                
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
