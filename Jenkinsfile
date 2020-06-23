pipeline{
agent none

stages{
stage('Clean Workspace'){
 steps {
        cleanWs()
      }
	  }
}
 stage('Git Checkout'){
steps {
        checkout scm
    }
}
}
