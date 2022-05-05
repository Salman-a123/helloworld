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
                SUB='SBX'
                if [[ "$STR" == *"$SUB"* ]]; 
                then
                echo "True" 
                fi
                ''',returnStdout:true)
        echo " I am here :${bool}"
        if (bool=="True"){
            echo "Mycode is working"
        else {
            echo "My code is not working"
        }
        }
            
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
