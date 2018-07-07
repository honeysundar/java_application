
    agent {
    node {
        label 'docker'
        customWorkspace '/var/lib/jenkins'
    }
}

pipeline {
    agent { docker 'maven:3-alpine' } 
    stages {
        stage('Example Build') {
            steps {
                sh 'mvn -B clean verify'
            }
        }
    }
}

