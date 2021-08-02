pipeline {
    agent any
    stages {
        stage('Setup parameters') {
            steps {
                script { 
                    properties([
                        parameters([
                            string(
                                defaultValue: '', 
                                name: 'BaseBranchName', 
                                trim: true
                            ),
                            string(
                                defaultValue: '', 
                                name: 'CommitID', 
                                trim: true
                            )
                        ])
                    ])
                }
            }
        }
        stage('CherryPick'){
            steps {
                script{
                    print "${params.BaseBranchName}"
                    print "${params.CommitID}"
                    sh """
                    git --version
                    git checkout ${params.BaseBranchName}
                    git cherry-pick ${params.CommitID}
                    git push
                    git checkout develop
                    git merge ${params.BaseBranchName}
                    """
                }
            }
        }
    }   
}
