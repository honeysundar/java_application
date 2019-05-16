pipeline {
    agent any

    stages {
        stage('Build') {
           
            steps {
                sh '/usr/bin/mvn package'
                
                  }
                      }
        stage('build docker image'){
            agent any
            steps {
            echo 'build docker image'
            }
        }
       
       
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
