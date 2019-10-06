pipeline {
    agent any
    tools { 
        maven 'Maven_Home' 
        jdk 'jdk1.8.0_221' 
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    pwd "PATH = ${PATH}"
                    pwd "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }

        stage ('Build') {
            steps {
                echo 'This is a minimal pipeline.'
            }
        }
    }
}
