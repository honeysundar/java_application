pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    mvn package
                '''
            }
        }
        Stage('Upload') {
            step {
                rtUpload  (
    serverId: "jfrog",
    spec:
        """{
          "files": [
            {
              "pattern": "target/*war",
              "target": "jave_app/,
            }
         ]
        }"""
)

                }
                        }
           
            }
}

