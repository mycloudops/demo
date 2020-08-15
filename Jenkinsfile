pipeline {
  agent any
  environment{
     BRANCH = "${env.BRANCH_NAME}"
  }
  parameters {
    choice(name: 'terrafrom_mode',
      choices: 'init\ndestroy',
      description: 'It will decide terraform mode choice')
  stages{
        stage('Build Docker Image'){
            steps{
                sh '''
                oFN=sfdsd
                nFN=sfdsd
                oldSHC=afkjsdkj1232nkjsd
                SHC=afkjsdkj1232nkjbd
                if [ $params.terrafrom_mode == init ]
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
