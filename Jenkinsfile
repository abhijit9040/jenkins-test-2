
pipeline {
    agent any
    tools {
        maven 'maven'  
    }
    stages {
        stage('Build') {
            steps {
                bat 'mvn  -DskipTests clean package'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Deliver'){
            steps{
                script{
                       bat './scripts/deliver.sh'
                }
            }
        }
       
        }
        
    }
