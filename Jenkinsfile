pipeline {
    agent none 
    stages {
        stage('Example Build') {
            agent none 
            steps {
                def listing = sh script: 'ls -la /', returnStdout:true
                echo "${listing}"
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
