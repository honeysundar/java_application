pipeline { 
    agent any  
    stages { 
        stage('checkout') { 
            scm checkout
        }
        stage('build') { 
            mvn clean install
        }
    }
}
