pipeline {
    agent any

    stages {
        stage('Build') {
                agent {
                        docker { image 'maven:3-alpine' }
                      }
            steps {
                sh 'mvn package'
                sh 'docker run -t java_app .'
                  }
                      }
        
       
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
