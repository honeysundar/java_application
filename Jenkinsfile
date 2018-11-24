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
       
       
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
