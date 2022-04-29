pipeline 
{
    agent any
    
  
   stages 
    {
       
        stage("git")
       {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main' , credentialsId:'git_credentials', url: 'https://github.com/soumya132/28apriljavacode.git'

              
            }
        }
        stage("build")
       {
            steps 
           {
                // Get some code from a GitHub repository
               //def mvnhome = tool name: 'apache-maven-3.6.1', type: 'maven'
                bat "mvn package"

              
            }
        }
       stage('SonarQube analysis')
       {
           steps
           {
             withSonarQubeEnv(credentialsId: 'mishratoken', installationName: 'sonarqube') 
               { 
                    bat 'mvn sonar:sonar'
               }
    
           }
  
    }
}
    
}
