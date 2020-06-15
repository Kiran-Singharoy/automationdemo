pipeline {
 
  stages{
    
    stage('Cloning Git') {
        checkout scm
    }
    stage('Install dependencies') {
         agent { 'NodeJS'}
        steps{
            sh 'npm install'
            echo "Modules installed"
        }
    }
  }
}
