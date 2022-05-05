pipeline {
    agent none 
    stages {
        stage('Check') {
    steps {        
        script {
            Boolean bool = fileExists 'NewFile.txt'
            if (bool) {
                println "The File exists :)"
            } else {
                println "The File does not exist :("
            }   
        }         
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
