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
            stage('Upload'){
                curl -u admin:password -T target/grants.war "http://ec2-54-242-220-114.compute-1.amazonaws.com:8081/artifactory/chakri_java_app/"
            }
            }
}
