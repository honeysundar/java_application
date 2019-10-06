library identifier: 'shared-lib@master', retriever: modernSCM(
        [$class: 'GitSCMSource',
         remote: 'https://github.com/honeysundar/shared-lib.git',
         credentialsId: 'git'])
pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                hello.printHello()
            }
        }
        stage('Test') { 
            steps {
                sh 'echo "mvn test"'
            }
        }
        stage('Deploy') { 
            steps {
                sh 'echo "Deploy step"'
            }
        }
    }
}
