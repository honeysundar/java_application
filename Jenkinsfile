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
              script {
              dockerImage = docker.build("honeysundar/java_app_sra_ninika")
                }
                 }
       }
       stage('Deploy Image') {
           agent any
          steps{
          script {
              withDockerRegistry([ credentialsId: "docker-hub", url: "" ])
             {
                 dockerImage.push("${env.BUILD_NUMBER}")
                 dockerImage.push("latest")
            }
    }
  }
}    
                
             
        }
        
    }
