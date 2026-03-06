pipeline {
    agent none


    stages {
        stage ('Stage 1') {

            agent { label 'slave1' }
            
            steps {
                sh 'sleep 5'
                echo "This is the stage1"
            }
        }
        stage ('stage 2') {

            agent { label 'slave2' }

            steps {
                sh ''' 
                #!/bin/bash
                pwd
                ls -lrt
                sleep 5
                '''
                echo "This is stage 2"
            }
        }
    }
}

