pipeline {
    agent any
    stages {
        stage('Build') { 
             steps {
                 sh 'export MAVEN_HOME=/usr/local/bin/mvn'
                 sh  'export PATH=$PATH:$MAVEN_HOME/bin'
                 sh 'mvn --version'
                 sh 'mvn clean package'
        }
        }
    }
}
