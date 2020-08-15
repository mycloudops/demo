pipeline {
  agent any
  environment{
     BRANCH = "${env.BRANCH_NAME}"
  }
  parameters {
    choice(name: 'terrafrom_mode',
      choices: 'init\ndestroy',
      description: 'It will decide terraform mode choice')
  }
  stages{
        stage('Build Docker Image'){
            steps{
              if ( ${params.terrafrom_mode} == init ){
                sh label: '', script: 'echo "True"'
              }
              else{
              sh label: '', script: 'echo "False"'
              }
            }
        }
   }  
}
