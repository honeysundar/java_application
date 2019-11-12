pipeline {
    agent any
        stages {
            stage('Build') {
               steps {
                    git "https://github.com/DeepanVenkatesh/java_application"
                      }
                post {
                    always {
                            sh "mvn clean package"
                        }  
                }
                }
            stage('Parallel Test') {
                parallel {
                    steps {
                    echo " Testing Parallel Steps"
                    }    
                }
            }
        }
    
}
