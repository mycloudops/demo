pipeline {
  agent any
  environment{
     BRANCH = "${env.BRANCH_NAME}"
  }
  parameters {
    booleanParam(defaultValue: true, description: 'This is to select terraform apply or destroy.', name: 'apply')
  }
  stages{
        stage('Build Docker Image'){
            steps{
              if ("${params.apply}") {
                sh label: '', script: 'echo "True"'
              }
              else {
              sh label: '', script: 'echo "False"'
              }
            }
        }
   }  
}
