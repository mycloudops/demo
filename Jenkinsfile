pipeline {
  agent any
  parameters {[
    stringParam(defaultValue: '', name: 'BaseBranchName'),
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
