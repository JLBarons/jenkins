
pipeline {
  agent  any 

 
   stages {
    stage (‘Git’) {
      steps {
        sh 'git clone https://github.com/skscharr/ascii_cat.git '
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
