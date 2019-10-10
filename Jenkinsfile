pipeline { 
    agent { label 'slave' }
    stages {
        stage('Build') { 
            steps { 
                sh 'mvn package' 
            }
        }
        stage('Test'){
            steps {
                sh 'mvn test'
             
            }
        }
        
    }
}
