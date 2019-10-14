pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v $HOME/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn package'
            }
        }
        
        stage('SonarQube analysis') { 
             steps {
        withSonarQubeEnv('sonar,credentialsId: 'f3722f37d25c1a67a3e9ce140f995f74e1e74a9b'') { 
          sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.3.0.603:sonar'
        }
        }
        }
    }
}
