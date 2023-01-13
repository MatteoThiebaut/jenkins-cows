pipeline {
    agent any

    stages {
        stage('Package') {
            steps {
            	bat 'mvn clean'
                bat 'mvn package' 
                bat 'mvn compile' 
            }
        }
        
        stage('Publish') {
            steps {
                archiveArtifacts 'cowjar/target/*.jar'
                archiveArtifacts 'cowsay/target/*.jar'
            }
        }
        
    }
}
