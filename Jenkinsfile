pipeline {
    agent any
    stages {
        stage('Run Tests') {
            parallel {
                stage('Test On parallel') {
                    
                    steps {
                        sh 'echo thread 1'
                    }
                    post {
                        always {
                            sh ' echo post build'
                        }
                    }
                }
                stage('Test On Linux') {
                    
                    steps {
                        sh 'echo thread 2'
                    }
                    post {
                        always {
                            sh 'echo post build'
                        }
                    }
                }
            }
        }
    }
}
