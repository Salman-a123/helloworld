pipeline {
    agent none 
    stages {
        stage('Example Build') {
            agent none 
            steps {
                result=sh(script: """git log -1 --pretty=%B """,returnStatus: true)
            }
        }
        stage('Example Test') {
            agent none 
            steps {
                echo 'Hello, JDK'
                
            }
        }
    }
}
