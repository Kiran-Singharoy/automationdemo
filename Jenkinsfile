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
      sh 'npm run build'
      echo "Running npm build"
      sh 'pwd'
    }
  }
  stage('checking'){
    steps{
      sh 'cd /opt/jenkins'
      sh 'touch eai.txt'
    }
  }
}
}
 

