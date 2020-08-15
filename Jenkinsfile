pipeline {
  agent any
  environment{
     BRANCH = "${env.BRANCH_NAME}"
  }
  stages{
        stage('Build Docker Image'){
            steps{
                sh '''
                SHC=afkjsdkj1232nkjsd
                oldSHC=$(cat hashcode | xargs)
                if ( $SHC == $oldSHC )
                then
                echo "True"
                else
                echo "False"
                sed -i -e "s/$oldSHC/$SHC/g" hashcode
                cat hashcode
                echo "SCH replaced"
                git remote add central https://github.com/mycloudops/demo.git
                git config --global user.email "postbox.mywork@gmail.com"
                git config --global user.name "mcloudops"
                git add hashcode
                git commit -m "Jenkins commit"
                git push origin $BRANCH
                fi  
             '''   
            }
        }
   }  
}
