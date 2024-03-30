node{
  
stage('SCM Checkout')
  {
  git 'https://github.com/pulak1986/my-app-2021'
  }
stage('Compile-Package'){

  def mvn-home = tool name: 'maven-3', type: 'maven'
   sh "${mvn-home}/bin/mvn package"

    }
  
}
