
pipeline {
  agent { any }
  stages {
    stage (‘Git’) {
      steps {
       sh ‘mkdir cowpy’
       sh ‘pip install --install-option="--prefix=cowpy" cowsay’
  }
}
    stage (‘Build’) {
      steps {
       //Build the contents of repo
      sh 'cowsay test'
     }
}

  }
}
