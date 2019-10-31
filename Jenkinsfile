pipeline {
    agent any
    stages {
        stage('SonarQube analysis') { 
             steps {
                sh 'mvn clean install'
                withSonarQubeEnv('sonar') { 
                sh 'mvn sonar:sonar'
                }
        }
        }
        
    }
}
