pipeline {
    agent any 
    stages {
        stage('Check') {
    steps {        
        script {
  try {
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
                ''',returnStdout:true)
            
  } catch (Exception e) {
      echo 'Exception occurred: ' + e.toString()
      sh 'Handle the exception!'
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
