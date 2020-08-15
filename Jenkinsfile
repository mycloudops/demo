pipeline {
  agent any
  environment{
     BRANCH = "${env.BRANCH_NAME}"
  }
  parameters {
       booleanParam(name: 'apply'
         defaultValue: true,
         description: 'apply should be false')
       booleanParam(name: 'destroy'
         defaultValue: false,
         description: 'apply should be false')
  }
  stages{
        stage('Build Docker Image'){
            steps{
              if (params.apply) {
                sh label: '', script: 'echo "True"'
              }
              if (params.init) {
              sh label: '', script: 'echo "False"'
              }
            }
        }
   }  
}
