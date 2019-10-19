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
                sh 'mvn sonar:sonar -Dsonar.login=787fbc118c2a5e9544d73adbdb3f531a73d61ffb'
        }
        }
        
    }
}
