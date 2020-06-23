pipeline{
agent{ label "NodeJS" }

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
