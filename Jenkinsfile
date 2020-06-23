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
      sh 'touch /opt/jenkins/check.txt'
      sh 'pwd >> /opt/jenkins/check.txt'
       
    }
  }
  stage('Package Build'){
    steps
    {
        sh "tar -zcvf bundle.tar.gz dist/automationdemo/"
    }
  }
    stage('Artifacts Creation') {
      steps{
        fingerprint 'bundle.tar.gz'
        archiveArtifacts 'bundle.tar.gz'
        echo "Artifacts created"
        }
    }

    stage('Stash changes') {
        stash allowEmpty: true, includes: 'bundle.tar.gz', name: 'buildArtifacts'
    }
  
}
}
 

