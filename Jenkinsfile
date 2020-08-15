pipeline {
  agent any
  environment{
     BRANCH = "${env.BRANCH_NAME}"
  }
  parameters {
    choice(name: 'terrafrom_mode',
      choices: 'init\ndestroy',
      description: 'It will decide terraform mode choice')
  }
  stages{
        stage('Build Docker Image'){
            steps{
                sh '''
                mode=$params.terrafrom_mode
                oFN=sfdsd
                nFN=sfdsd
                oldSHC=afkjsdkj1232nkjsd
                SHC=afkjsdkj1232nkjbd
                if [ $mode == init ]
                then
                echo "True"
                else
                echo "False"
                fi  
             '''   
            }
        }
   }  
}
