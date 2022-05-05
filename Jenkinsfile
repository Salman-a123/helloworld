pipeline {
    agent any 
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
            agent any 
            steps {
                echo 'Hello, JDK'
                
            }
        }
    }
}
