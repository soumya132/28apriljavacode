pipeline {
    agent any
    
  
   stages {
        stage("git") {
            steps {
                // Get some code from a GitHub repository
                git credentialsId:'git_credentials', url: 'https://github.com/soumya132/28apriljavacode.git'

              
            }
        }
        stage("build") {
            steps {
                // Get some code from a GitHub repository
                sh 'mvn package'

              
            }
        }
    }
}
