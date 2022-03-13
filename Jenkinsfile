pipeline {
    
    agent any
    
    stages {
        stage ('Fetch code') {
            steps {
                git branch: 'main', url:'https://github.com/rajroj2014/devops-udemy-vproject.git'
            }
        }
        stage ('Build') {
            steps {
                sh 'mvn install'
            }
        }
        stage ('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Code Ananlysis'){
            steps {
                sh 'mvn checkstyle:checkstyle'
            }
        }
       
    }
}
