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
                stage('UT Test On parallel') {
                    
                    steps {
                        sh 'echo thread 1'
                    }
                    post {
                        always {
                            sh ' echo post build'
                        }
                    }
                }
            }
        }
        }
}
