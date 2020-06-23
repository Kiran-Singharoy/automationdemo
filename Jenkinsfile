pipeline{
agent{ label "NodeJS" }

stages{
  
/*  stage('Clean Workspace'){
 steps {
        cleanWs()
      }
	  }*/

 stage('Git Checkout'){
steps {
       git 'https://github.com/Kiran-Singharoy/automationdemo.git'
      
    }
}
  stage('Install npm dependencies'){
    steps{
      sh 'npm install'
            echo "Modules installed"
         }
      }
  stage('NPM build'){
    steps{
      sh 'npm build'
      echo "Running npm build"
    }
  }
}
}
 }

