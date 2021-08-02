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
                    git remote add origin git@github.com:mycloudops/demo.git
                    git checkout ${params.BaseBranchName}
                    git push origin master
//                     git cherry-pick ${params.CommitID}
//                     git checkout develop
//                     git merge ${params.BaseBranchName}
                    """
                }
            }
        }
    }   
}
