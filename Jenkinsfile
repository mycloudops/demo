pipeline {
  agent any
  environment{
     BRANCH = "${env.BRANCH_NAME}"
  }
  stages{
        stage('Build Docker Image'){
            steps{
                sh '''
                oldSHC=$(cat /home/hashcode | xargs)
                SHC="afkjsdkj1232nkjsd"
                if ( $SHC == $oldSHC )
                echo "True"
                else
                echo "False"
                sed -i -e "s/$oldSHC/$SHC/g" /home/hashcode
                cat hashcode
                echo "SCH replaced"
                fi  
             '''   
            }
        }
   }  
}
