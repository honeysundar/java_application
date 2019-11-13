pipeline {
    agent any
    stages {
        stage('Build') { 
             steps {
                sh 'mvn clean package'
        }
        }
        stage('SonarQube analysis') { 
             steps {
                withSonarQubeEnv('sonar') { 
                sh 'mvn sonar:sonar'
                }
        }
        }
         stage('push to jfrog') { 
             steps {
                rtUpload (
                serverId: 'jfrog',
                spec: '''{
                    "files": [
                {
                "pattern": "target/*.war",
                "target": "java_app/"
                }
         ]
    }''',
                )
                }
        }
        }
        
    }
