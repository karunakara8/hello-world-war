pipeline {
    agent { label 'builtinnode' }
    stages {
        stage ('build') {
            steps {
                sh 'mvn package'
                sh 'ls'
                sh 'pwd'
            }
        }
      stage ('deploy') {
            steps {
                sh 'pwd'
                sh 'hostname -i'
                sh 'sudo cp -R /var/lib/jenkins/workspace/myfirstpipeline/target/hello-world-war-1.0.0.war /opt/tomcat/webapps/'
                sh 'sudo sh /opt/tomcat/bin/shutdown.sh'
                sh 'sleep 2'
                sh 'sudo sh /opt/tomcat/bin/startup.sh'
            }
        }
    }
}
