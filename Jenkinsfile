node{
  
stage('SCM Checkout')
  {
  git 'https://github.com/pulak1986/my-app-2021'
  }
stage('Compile-Package'){

  def mvnHome = tool name: 'maven-3', type: 'maven'
   sh "${mvnHome}/bin/mvn package"

    }
  
}
