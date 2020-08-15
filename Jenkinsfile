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
                sed -i 's/$oldSHC/$SHC/gI' hashcode
                echo "SCH replaced"
                fi  
             '''   
            }
        }
   }  
}
