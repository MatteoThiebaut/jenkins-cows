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
                    repository: 'RepositoryName',
                 credentialsId: 'CredentialsId',
                 artifacts: [
                        [artifactId: projectName,
                       classifier: '',
                         file: 'my-service-' + version + '.jar',
                            type: 'jar']
        ]
     )
                    }
    }
}
}

