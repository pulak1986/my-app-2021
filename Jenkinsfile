pipeline {

  agent {
    label 'Linux-Slave-01'
  }
stages{ 
stage('SCM Checkout'){
  steps
  {
  git 'https://github.com/pulak1986/my-app-2021'
  }
  }
stage('Compile-Package'){

  steps
  {

  def mvnHome = tool name: 'maven-3', type: 'maven'
   sh "${mvnHome}/bin/mvn package"
  }
    }
  stage('Email Notification'){

    steps
    {
       mail bcc: '', body: '''Hi,

Welcome to Jenkins alerts

Thanks and Regards
Pulak kar''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'kar.pulakk@gmail.com'
  }
  }
  stage('Slack Notification') {
   steps {
    slackSend baseUrl: 'https://hooks.slack.com/services/', channel: 'jenkins-pipeline', color: 'good', message: 'Welcome to Jenkins Slack', teamDomain: 'Academic', tokenCredentialId: 'slack-demo'
  }
}
}
}
