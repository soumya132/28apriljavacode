pipeline {
    agent any
    tools {
        maven 'apache-maven-3.6.1'
        
    }
  
   stages {
       
       stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }
       
        stage("git") {
            steps {
                // Get some code from a GitHub repository
                git credentialsId:'git_credentials', url: 'https://github.com/soumya132/28apriljavacode.git'

              
            }
        }
        stage("build") {
            steps {
                // Get some code from a GitHub repository
               //def mvnhome = tool name: 'apache-maven-3.6.1', type: 'maven'
                sh "mvn package"

              
            }
        }
    }
}
