pipeline {
    agent any
    stages {
        stage('Build'){
            steps{
                sh 'mvn clean package'
            }
            post{
                success{
                    echo"Archiving the artifacts"
                    archiveArtifacts artifacts: "**/target/*.war"
                }
            }
        }
        stage('deploy to tomcat sever')
    }
