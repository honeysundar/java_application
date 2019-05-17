pipeline {
    agent any
    stages {
        
    stage('Build') {
           steps {
            
                 
                sh 'mvn clean install test'
            
        } 
       
   }
   
      
   }  
    }
    post {
        always {
            echo 'I have finished and deleting workspace'
            deleteDir() 
        }
        success {
            echo 'Job succeeeded!'
        }
        unstable {
            echo 'I am unstable :/'
        }
        failure {
            echo 'I failed :('
        }
        changed {
            echo 'Things were different before...'
        }
    }
}
