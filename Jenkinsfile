pipeline {
    agent any
    parameters {
        string(name: 'Greeting', defaultValue: 'Unimoni', description: 'Greetigns')
        string(name: 'unimoni_env', defaultValue: 'DEV', description: 'Greetigns')
    }
    stages {
        stage('Example') {
            steps {
                echo "${params.Greeting} World!"
                 echo "${params.unimoni_env} World!"
            }
        }
    }
}
