pipeline {
    agent any
    stages {
        
        stage('push to jfrog') { 
             steps {
                rtUpload (
                serverId: 'jfrog',
                spec: '''{
                    "files": [
                {
                "pattern": "target/*.war",
                "target": "jave_app/"
                }
                ]
                    }''',
                    )
                }
        }
        }
        
    }
