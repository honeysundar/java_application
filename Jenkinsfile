pipeline {
   agent any
   parameters {
        string(choices: ['DEV', 'PROD'],name: 'ENV', defaultValue: 'DEV', description: 'How should I greet the world?')
        choice(choices: ['US-EAST-1', 'US-WEST-2'], description: 'What AWS region?', name: 'region')
    }
    stages {
       
        stage('Build') {
           
           agent { 
               label 'dev'
            }
            steps {
                echo 'Building..'
                 sh 'mvn package'
            }
        }
       
   
        stage('Deploy') {
           agent { 
               label 'dev'
            }
            
            steps {
                
                sh 'sudo apt update -y'
                sh 'sudo apt install tomcat8 -y'
                sh 'sudo apt install tomcat8-admin -y'
                sh 'sudo apt install tomcat8-user -y'
                sh 'sudo cp /home/ubuntu/workspace/Deployment/target/grants.war /var/lib/tomcat8/webapps/'
                sh 'sudo cp /home/ubuntu/workspace/Deployment/tomcat-users.xml /etc/tomcat8/'
                sh 'sudo service tomcat8 restart'
            }
        }
    }
}
