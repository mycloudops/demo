pipeline {
  agent any
  stages{
        stage('Setup parameters') {
            steps {
                script { 
                  properties([
                  parameters ([
                    string(defaultValue: '', name: 'BaseBranchName'),
                    string(defaultValue: '', name: 'CommitID')
                  ])
                  ])
                }
            }
        }
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
