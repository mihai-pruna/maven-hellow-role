pipeline{
    agent any
    // agent { label jenkins_node }

    tools {
         maven 'maven'
         // jdk 'java'
    }

    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github_access', url: 'https://github.com/mihai-pruna/java-hello-world-with-maven.git']]])
            }
        }
        stage('build'){
            steps{
               // bat 'mvn package'
                sh 'mvn package'
            }
        }
    }
}
