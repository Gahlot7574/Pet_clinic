pipeline {
    agent any
    
    tools {
        jdk 'jdk11'
        maven 'maven3'
    }

    environment {
        SCANNER_HOME = tool 'sonar-scanner'
    }
    
    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Raghava0684/Petclinic-project.git'
            }
        }
        
        stage('Mvn compile') {
            steps {
                sh 'mvn compile'
            }
        }
        
        stage('Mvn package') {
            steps {
                sh 'mvn package'
            }
        }
    
    }
}
