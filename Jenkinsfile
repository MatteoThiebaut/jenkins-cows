pipeline {
    agent any

    stages {
        stage('Package') {
            steps {
            	bat 'mvn clean'
                bat 'mvn package' 
            }
        }
        
        stage('Publish') {
            steps {
                archiveArtifacts 'cowjar/target/*.jar'
                archiveArtifacts 'cowsay/target/*.jar'
                archiveArtifacts 'cowsay-parent/target/*.jar'
            }
        }
        
    }
}
