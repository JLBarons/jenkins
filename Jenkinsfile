username = 'JENKINSUSERNANENENENENE'

pipeline {
  agent  any 

 
   stages {
    stage (‘Git’) {
      steps {
     sh 'rm -rf fortune'
     sh 'rm -rf fortune_bin'
     sh 'git clone https://github.com/bmc/fortune.git' 

     }
  }


   stage ('Build') {
    steps { 
       dir('fortune') {
          sh 'python3 setup.py install --prefix=../fortune_bin'
         }

       echo "user variable ${username}"
 
       }
     }  
  stage ( 'Cowsay') {
    steps{
     sh 'cowsay  ${USER}  ${GIT_BRANCH}'

    }
}


   }

  }
