pipeline {
    agent none 
    stages {
        stage('Example Build') {
            agent none 
            steps {
                sh '''#!/bin/bash
                echo "hello world" 
                '''
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
