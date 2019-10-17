pipeline {
    agent any
    tools { 
        maven 'Maven_Home' 
        jdk 'jdk1.8.0_221' 
    }
    stages {
        
        stage('checkout') {
        git 'https://github.com/skhare994/jenkins-git-integration.git'
            
        }
        
        stage ('Initialize') {
            steps {
                bat '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }

        stage ('Build') {
            steps {
                bat 'mvn -Dmaven.test.failure.ignore=true install' 
            }
            post {
                success {
                     echo 'This is a minimal pipeline...' 
                }
            }
        }
        
        stage ('Test') {
            steps {
                bat 'mvn install' 
            }
        }
    }
}
