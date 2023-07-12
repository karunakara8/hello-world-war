pipeline {
    agent { label 'builtinnode' }
    stages {
        stage ('build') {
            steps {
                sh 'mvn package'
                sh 'ls'
            }
        }
    
    }
}
