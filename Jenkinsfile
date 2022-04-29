pipeline {
    agent any
    
  
   stages {
       
        stage("git") {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main' , credentialsId:'git_credentials', url: 'https://github.com/soumya132/28apriljavacode.git'

              
            }
        }
        stage("build") {
            steps {
                // Get some code from a GitHub repository
               //def mvnhome = tool name: 'apache-maven-3.6.1', type: 'maven'
                bat "mvn package"

              
            }
        }
       stage('SonarQube analysis') {
           steps{
    withSonarQubeEnv(credentialsId: 'e8ad8951d1fac528db71ac15d7d545774f270ee0', installationName: 'sonarqube') { // You can override the credential to be used
      bat 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.7.0.1746:sonar'
    }
           }
  }
    }
}
