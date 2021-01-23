
pipeline { 
    agent any 
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') { 
            steps { 
                sh 'echo "test version"' 
            }
        }
        stage('Test'){
            steps {
                sh 'echo "test stage"'
            }
        }
        
    }
}
