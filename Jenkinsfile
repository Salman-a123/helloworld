pipeline {
    agent none 
    stages {
        stage('Example Build') {
            agent none 
            steps {
                echo 'Hello, Maven'
                echo "I am here"
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
