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
              echo "Trying ${params.apply}"
            }
        }
   }  
}
