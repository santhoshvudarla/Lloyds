pipeline {
    agent { label 'Buildgroup' }
    environment {
        VARVAL = 'global'
    }
    stages {
        stage('Stage1') {
            environment {
                VARVAL = 'local'
            }
            steps {
                sh "echo 'Your name: $VARVAL'"
            }
        }
        stage('Stage2') {
            steps {
                echo env.VARVAL
            }
        }
    }
}
