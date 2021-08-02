pipeline {
  agent any
  parameters {[
    booleanParam(defaultValue: true, description: 'This is to select terraform apply or destroy.', name: 'apply')
    stringParam(defaultValue: '', name: 'BaseBranchName')
    stringParam(defaultValue: '', name: 'CommitID')
  ]}
  stages{
        stage('CherryPick'){
          steps{
              git checkout params.BaseBranchName
              git cherry-pick params.CommitID
              git checkout develop
              git merge params.BaseBranchName
            }
        }
    }  
}
