pipeline {
   agent any
   parameters {
        string(name: 'ENV', defaultValue: 'DEV', description: 'How should I greet the world?')
    }
    stages {
       
        stage('Build') {
           
           agent { 
               label 'docker'
            }
            steps {
                echo 'Building..'
                 sh 'mvn package'
            }
        }
       
   
        stage('Deploy') {
           agent { 
               label 'docker'
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
