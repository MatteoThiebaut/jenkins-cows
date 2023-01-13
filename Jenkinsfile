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
         stage("Publish to Nexus Repository Manager") {
            steps {
                   nexusArtifactUploader(
                    nexusVersion: 'nexus3',
                    protocol: 'http',
                    nexusUrl: 'http://localhost:8081/repository/cow/',
                    groupId: 'com.example',
                    version: version,
                    repository: 'cow',
                 credentialsId: 'admin',
                 artifacts: [
                        [artifactId: 'cowjar',
                       classifier: '',
                         file: 'cowjar-1.1.1-SNAPSHOT.jar',
                            type: 'jar']
                                ]
                        )
                    }
        }
    }
}

