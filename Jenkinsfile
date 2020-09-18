pipeline {
  
    agent none
    stages {
        stage('Build') { 
            agent any
             steps {
                sh 'mvn install'
            }
            }
       
       stage ('dockerization') {
           agent any
            steps{
              sh 'docker build -t honeysundar/java_sra_007 .'
                 }
       }
       stage('Deploy Image') {
           agent any
          steps{
          
              withDockerRegistry([ credentialsId: "docker-hub", url: "" ])
             {
                 sh 'docker push honeysundar/java_sra_007'
            }
    
  }
}    
                
             
        }
        
    }
