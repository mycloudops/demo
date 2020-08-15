pipeline {
  agent any
  environment{
     BRANCH = "${env.BRANCH_NAME}"
  }
  properties([
     parameters([
       booleanParam(
         defaultValue: true,
         description: 'apply should be false',
         name: 'apply'
       ),
       booleanParam(
         defaultValue: false,
         description: 'destroy should be true',
         name: 'destroy'
       ),
     ])
   ])
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
