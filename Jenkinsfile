pipeline {
    agent any
    parameters {
        
        booleanParam(defaultValue: true, description: 'Dev ENV', name: 'Deployment ENV')
    
    }
    stages {
        stage('Example') {
            steps {
                echo "${params.Greeting} World!"
            }
        }
    }
}
