pipeline {
    agent any

    stages {
        stage ('STAGE!') {
            steps {
                echo "This is stage1 running"
                sh 'sleep 5'
            }
        }

        stage ('PARALLEL TESTING') {
            parallel {
                stage('WINDOWS TESTING') {
                    steps {
                        echo "This is WINDOWS testing running"
                        sh 'sleep 5'
                    }
                }

                stage ('MACOS TESTING') {
                    steps {
                        echo "This is MACOS running"
                        sh 'sleep 5'
                    }
                }
            }
        }

        stage ('FINAL') {
            steps {
                echo "THis is final stage"
                sh 'sleep 5'
            }
        }
    }
}