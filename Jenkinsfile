node
{

  stage('SCM Check out ')
  {
    git 'https://github.com/soumya132/28apriljavacode.git'
  }
  stage('compile and package')
  {
    sh 'mvn package'
  }
}
