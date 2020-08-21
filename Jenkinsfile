
pipeline {
  agent  any 

 
   stages {
    stage (‘Git’) {
      steps {

     }
  }


   stage ('Build') {
    steps { 
      sh 'printenv'
     }  
 
   stage ( 'Cowsay') {
      sh 'cowsay ${env.GIT_BRANCH}'
    }
  }


   }

 }
