pipeline {
    agent any
    tools { 
        maven 'Maven_Home' 
        jdk 'jdk1.8.0_221' 
    }
    stages {
        stage ('Initialize') {
            steps {
                bat '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }
    }
}
