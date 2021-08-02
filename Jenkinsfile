pipeline {
  agent any
  parameters ([
    string(defaultValue: '', name: 'BaseBranchName'),
    string(defaultValue: '', name: 'CommitID')
  ])
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
