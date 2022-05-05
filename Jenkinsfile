pipeline {
    agent any 
    stages {
        stage('Example Build') {
            agent any 
            steps {
                sh '''#!/bin/bash
                echo "hello world" 
                '''
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
