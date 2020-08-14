pipeline {
  agent any
    environment{
        $enableVersion = Version()
    }
  stages{
        stage('Build Docker Image'){
            steps{
                sh '''
                if [ $enableVersion == true ]
                then
                echo "enable version"
                else
                echo "disable version"
             '''   
            }
        }
   }  
}  
def Version(){
    def source_code_hash  = "nRC9RyWtg2Mh9xUCG+vt9F+LrYqOncRwnfOA7OEo5ks="
    def old_source_code_hash = source_code_hash
    if (old_source_code_hash != source_code_hash)
    return false
    else
    return true
}
