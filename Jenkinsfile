
pipeline { 
    agent any 
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') { 
            steps { 
                sh 'java --version' 
            }
        }
        stage('Test'){
            steps {
                sh 'echo "test stage"'
                junit 'reports/**/*.xml' 
            }
        }
        
    }
}
