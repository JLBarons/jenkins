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
     username = 'builduser'
    steps { 
      sh 'printenv'
      sh "rm -rf /tmp/${username}"
      dir("./${username}") {
         sh "python setup.py build"
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
