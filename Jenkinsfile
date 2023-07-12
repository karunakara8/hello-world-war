pipeline {
    agent { label 'builtinnode' }
    stages {
        stage ('build') {
            steps {
                sh 'mvn package'
                sh 'ls'
            }
        }
        stage ('deploy') {
            steps {
                sh 'pwd'
                sh 'hostname -i'
                sh 'sudo cp -R /hello-world-war-null.war /opt/tomcat/webapps/'
                sh 'sudo sh /opt/tomcat/bin/shutdown.sh'
                sh 'sleep 2'
                sh 'sudo sh /opt/tomcat/bin/startup.sh'
            }
        }
    }
}
