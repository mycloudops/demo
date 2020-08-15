pipeline {
  agent any
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
                sed 's/$oldSHC/$SHC/g' hashcode
                cat hashcode
                echo "SCH replaced"
                fi  
             '''   
            }
        }
   }  
}
