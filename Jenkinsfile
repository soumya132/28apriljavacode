node
{

  stage("git") {
            steps {
                // Get some code from a GitHub repository
                git credentialsId:'git_credentials', url: 'https://github.com/soumya132/28apriljavacode.git'

              
            }
        }
  stage('compile and package')
  {
    sh 'mvn package'
  }
}
