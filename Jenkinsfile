pipeline {
    agent any 
    stages {
        stage('Check') {
    steps {        
        script {
            def bool = sh (script:
                '''#!/bin/bash
                STR='https://ioi-toolchain.vwgroup.com/jenkins/job/E3_ADM/job/SBX/job/Adnan/job/e3_comp_cryptolib/'
                SUB='SBX'
                if [[ "$STR" == *"$SUB"* ]]; 
                then
                exit 0
                else
                # 1 = false
                exit 1
                fi
                ''',returnStdout:true)
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
