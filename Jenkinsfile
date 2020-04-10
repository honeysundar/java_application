pipeline {
    agent any
    stages {
        stage('Run Tests') {
            parallel {
                stage('UT Test On parallel') {
                    
                    steps {
                        sh 'echo thread 1'
                        sh 'sleep 10'
                    }
                    post {
                        always {
                            sh ' echo post build'
                        }
                    }
                }
                stage('IT Test On parallel') {
                    
                    steps {
                        sh 'echo thread 2'
                        sh 'sleep 10'
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
