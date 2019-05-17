pipeline {
    agent any
    
    stages {
        stage ('Initialize') {
          
           
           steps {
                
    sh "mvn package"
}
                
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
