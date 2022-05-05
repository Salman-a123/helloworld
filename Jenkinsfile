pipeline {
    agent none 
    stages {
        stage('Check') {
    steps {        
        script {
            def bool = sh (script:
                '''#!/bin/bash
                STR='https://ioi-toolchain.vwgroup.com/jenkins/job/E3_ADM/job/SBX/job/Adnan/job/e3_comp_cryptolib/'
                SUB='Stx'
                if [[ "$STR" == *"$SUB"* ]]; 
                then
                return 0
                else
                # 1 = false
                return 1
                fi
                ''',returnstatus:true)
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
