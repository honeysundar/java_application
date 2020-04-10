pipeline {
    agent any
    parameters {
        string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I greet the world?')
        choice{
           choices: 'Box\nOneDrive\nSharePointOnline\nGmail\nGDrive\nGenericS3',
           defaultValue: 'box', 
           description:  'Connector to build',
           name: 'On_Cloud_Devices_To_Test'
         }
    }
    stages {
        stage('Example') {
            steps {
                echo "${params.Greeting} World!"
            }
        }
    }
}
