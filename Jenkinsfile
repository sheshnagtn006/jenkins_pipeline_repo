pipeline {
    agent any

    
    stages {
        stage ('Stage 1') {
            steps {
                sh 'sleep 5'
                echo "This is the stage1"
            }
        }
        stage ('stage 2') {
            step {
                sh ''' 
                #!/bin/bash
                pwd
                ls-lrt
                sleep 5
                '''
                echo "This is stage 2"
            }
        }
    }
}