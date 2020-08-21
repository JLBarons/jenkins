username = 'testjenkinsuser'
pipeline {
  agent  any 

 
   stages {
    stage (‘Git’) {
      steps {
       sh 'git clone https://github.com/skscharr/ascii_cat.git' 
     }
  }


   stage ('Build') {
    steps { 
      sh 'printenv'
      dir('./acsii_cat') {
         sh "python setup install --prefix=/tmp/${username}"
        }
     }  
} 
   stage ( 'Cowsay') {
     steps {
     sh 'cowsay ${env.GIT_BRANCH} test2'
    }
  }


   }

 }
