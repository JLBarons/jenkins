pipeline {
  agent  any 

  stages {
    stage (‘Git’) {
      steps {
      sh 'git clone https://github.com/bmc/fortune.git' 

     }
  }


   stage ('Build') {
    steps { 
       dir('fortune') {
          sh 'python setup.py install --prefix=../fortune_bin'
         }

       }
     }  


   }

  }
