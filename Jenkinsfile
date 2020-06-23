pipeline{
agent none

stages{
stage('Clean Workspace'){
  
 steps {
        cleanWs()
      }
	  }

 stage('Git Checkout'){
steps {
       git 'https://github.com/Kiran-Singharoy/automationdemo.git'
      
    }
}
}
}
