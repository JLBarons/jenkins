pipeline {
  agent  any 

  stages {
    stage (‘Git’) {
      steps {
      sh 'printenv'
      echo "RUnning ${env.BUILD_ID} on ${env.JENKINS_URL} branch ${env.GIT_BRANCH}"
    }
  }


   stage ('Stage2') {
     
     def username = 'Jenkins'
     echo "hello ${username}"

     }  


   }

  }
