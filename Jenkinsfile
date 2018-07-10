pipeline {
    
agent { label 'docker' }
    
    
  
    stages {
        
        stage('Checkout') {
            steps {
        checkout scm
            }
    }
        stage('Build') {
            steps {
                echo 'Building..'
                 sh 'mvn package'
            }
        }
        
        
        stage('Decesion making deployment') {
            input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "sundar"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                }
            }
            steps {
                echo "Hello, ${PERSON}, nice to meet you."
            }
        }
        
        
        
        stage('Deploy') {
            steps {
                sh 'sudo apt update -y'
                sh 'sudo apt install tomcat8 -y'
                sh 'sudo apt install tomcat8-admin -y'
                sh 'sudo apt install tomcat8-user -y'
                sh 'sudo cp /root/grants.war /var/lib/tomcat8/webapps/'
                sh 'sudo cp /root/java_application/tomcat-users.xml /etc/tomcat8/'
                sh 'sudo service tomcat8 restart'
            }
        }
    }
}
