username = 'testjenkinsuser'
pipeline {
  agent  any 

 
   stages {
    stage (‘Git’) {
      steps {
       sh "rm -rf ${username}"
       sh "git clone https://github.com/skscharr/ascii_cat.git ${username}"  
     }
  }


   stage ('Build') {
    steps { 
      sh 'printenv'
      sh "rm -rf /tmp/${username}"
      dir('./acsii_cat') {
         sh "python setup.py install --prefix=/tmp/${username}"
        }
     }  
} 
   stage ( 'Cowsay') {
     steps {
     sh "cowsay ${env.GIT_BRANCH} test2"
    }
  }


   }

 }
