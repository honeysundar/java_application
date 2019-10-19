pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                sh 'mvn package'
            }
        }
        
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
