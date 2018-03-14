pipeline {
    agent any

    triggers {
        pollSCM('* * * * *')
    }

    stages{
        stage('Init'){
            steps {
                echo 'Testing...'
                sh '''pwd
                ls
                docker build -t martinliu/uptick-node:t1 .
                docker build -t martinliu/uptick-web:t1 Dockerfile.web'''
            }
        }
        stage('Build'){
            steps {
                echo 'Building...'
            }
        }
        
        stage('Deploy'){
            steps {
                echo 'Code Deployed....'
            }
        }
        
    }
}