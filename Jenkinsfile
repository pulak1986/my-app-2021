properties([parameters([choice(choices: 'master\nfeature-1\nfeature-2', description: 'Choose a Git branch to pull the code', name: 'branch')])])

node (label: 'Linux-Slave-01') {
   
   stage('SCM Checkout')
         {
    echo "pulling changes from the Branch ${param.branch}"
	  git url:'https://github.com/pulak1986/my-app-2021', branch : "${param.branch}"
         }

         }
