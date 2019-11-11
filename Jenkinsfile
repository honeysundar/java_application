pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test') { 
            steps {
                sh 'echo Test'
            }
        }
        stage('Deploy') { 
            steps {
                sh 'echo Deploy'
            }
        }
    }
}
