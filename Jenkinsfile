pipeline {
    agent any
    stages {
        stage('Setup parameters') {
            steps {
                script { 
                    properties([
                        parameters([
//                             choice(
//                                 choices: ['ONE', 'TWO'], 
//                                 name: 'PARAMETER_01'
//                             ),
//                             booleanParam(
//                                 defaultValue: true, 
//                                 description: '', 
//                                 name: 'BOOLEAN'
//                             ),
//                             text(
//                                 defaultValue: '''
//                                 this is a multi-line 
//                                 string parameter example
//                                 ''', 
//                                  name: 'MULTI-LINE-STRING'
//                             ),
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
    }   
}
// pipeline {
//   agent any
//   parameters {
//     string(defaultValue: '', name: 'BaseBranchName')
//     string(defaultValue: '', name: 'CommitID')
//   }
//   stages{
//         stage('CherryPick'){
//           steps{
//             git checkout ${params.BaseBranchName}
//             git cherry-pick ${params.CommitID}
//             git checkout develop
//             git merge ${params.BaseBranchName}
//             }
//         }
//     }  
// }
