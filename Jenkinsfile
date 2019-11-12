pipeline {
    agent any
    parameters {
        string(name: 'Greeting', defaultValue: 'Unimoni', description: 'Greetigns')
    }
    stages {
        stage('Example') {
            steps {
                echo "${params.Greeting} World!"
            }
        }
    }
}
