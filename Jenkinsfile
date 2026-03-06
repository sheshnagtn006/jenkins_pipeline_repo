pipeline {
    agent none // option given to choose the node on stage level and labels are mentioned in stage

    environment {
        DOCKER_USER = 'sheshnag'
        AWS_ACCESS_KEY = '09024095465156'
    }

    stages {
        stage ('Stage 1') {

            agent { label 'slave1' }  // stage1 run in slave1 labeled node
            
            steps {
                echo "DOCKER_USER: ${DOCKER_USER}"
                echo "AWS_ACCESS_KEY: ${AWS_ACCESS_KEY}"

                sh '''
                    env
                '''
            }
        }
    }
}