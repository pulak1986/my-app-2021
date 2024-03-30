node{
  
stage('SCM Checkout')
  {
  git 'https://github.com/pulak1986/my-app-2021'
  }
stage('Compile-Package'){

  def mvn-home = tool name: maven3 , type: Maven
   sh "${mvn-home}/bin/mvn package"

    }
  
}
