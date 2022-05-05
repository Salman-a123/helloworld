pipeline {
    agent none 
    stages {
        stage('Example Build') {
            agent none 
            steps {
                def result=sh(script: "git log -1 --pretty=%B | grep '\\[jenkins-full]'",returnStatus: true)
                echo "Build full flag: ${result}"
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
