pipeline { 
    agent any  
    stages { 
        stage('Build') { 
            steps { 
              // echo 'This is a minimal pipeline.'
                sh 'mvn clean install'
                sh 'docker build -t testBuild .'
                sh 'docker run -t testBuild'
                                
            }
        }
    }
}
