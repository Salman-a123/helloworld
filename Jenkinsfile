pipeline {
    agent any 
    stages {
        stage('Check') {
    steps {        
        script {
            def bool = sh (script:
                '''#!/bin/bash
                STR='https://ioi-toolchain.vwgroup.com/jenkins/job/E3_ADM/job/SBX/job/Adnan/job/e3_comp_cryptolib/'
                SUB='E10'
                echo "I am here"
                if [[ "$STR" == *"$SUB"* ]]; then
                echo "It's there."
                fi
                ''',returnStdout:true)
            if (bool) {
                println "Operation is performed :)"
                echo "This is the result:${bool}"
            } else {
                println "Operation is not performed :("
                echo "This is the result:${bool}"
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
