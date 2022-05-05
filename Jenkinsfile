pipeline {
    agent any 
    stages {
        stage('Check') {
    steps {        
        script {
            def bool = sh (script: "git log -1 --pretty=%B | grep '\\[jenkins-full]'",returnStatus: true) == 0
            if (bool) {
                println "Operation is performed :)"
                echo "This is the result:{bool}"
            } else {
                println "Operation is not performed :("
            }   
        }         
    }
    }   
        stage('Example Test') {
            agent any 
            steps {
                echo 'Hello, JDK'
                
            }
        }
    }
}
