pipeline {

    agent any

    

    parameters {
        booleanParam(name: "RELEASE",
                description: "Build a release from current commit.",
                defaultValue: false)
    }

    stages {

        stage("Build & Deploy SNAPSHOT") {
            steps {
                sh "mvn -B package"
            }
        }

       
    }

    post {
        always {
            deleteDir()
        }
    }
}
