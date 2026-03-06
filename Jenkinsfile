pipeline {
    agent none // option given to choose the node on stage level and labels are mentioned in stage

    parameters {
        string(name: 'NAME', defaultValue:, description: 'saying the name here')
        boolean(name: 'SKIP_TEST', description: 'want to skip test')
        choice(name: 'BRANCH', choices: ['master', 'stagging', 'prod'], description: '')
    }

    stages {
        stage ('Stage 1') {

            agent { label 'slave1' }  // stage1 run in slave1 labeled node
            
            steps {
                echo "NAME: ${params.NAME}"
                echo "SKIP_TEST: ${params.SKIP_TEST}"
                echo "BRANCH TO DEPLOY: ${params.BRANCH}"
            }
        }
    }
}