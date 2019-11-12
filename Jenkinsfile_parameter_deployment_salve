pipeline {
   agent { 
               label 'docker'
            }
   parameters {
        string(name: 'ENV', defaultValue: 'docker', description: 'How should I greet the world?')
    }
    stages {
        stage('Build') {
           agent { 
                label 'master'
            }
            steps {
                echo 'Building..'
                 sh 'mvn package'
            }
        }
       
   
        stage('Deploy') {
            
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
