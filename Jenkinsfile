pipeline { 
    agent any 
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
        stage('code coverage with sonar ') {
            steps {
                sh 'mvn org.sonarsource.scanner.maven:sonar'
            }
        }
    }
}
