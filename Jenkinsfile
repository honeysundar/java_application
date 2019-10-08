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
                withSonarQubeEnv('sonar')
                {
                sh 'mvn sonar:sonar -X'
                }
            }
        }
    }
}
