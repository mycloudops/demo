pipeline {
  agent any
  environment{
     BRANCH = "${env.BRANCH_NAME}"
  }
  parameters {
    booleanParam(defaultValue: true, description: 'This is to select terraform apply or destroy.', name: 'apply')
  }
  stages{
        stage('Apply'){
          when {
          expression {
                 return (params.apply)
          }
       }
          steps{
              echo "True"
            }
        }
    stage('Destroy'){
      when {
          expression {
                 return !(params.apply)
          }
      }
          steps{
              echo "False"
            }
        }
   }  
}
