pipeline {
  agent any
    environment{
        enableVersion = Version()
    }
  stages{
        stage('Build Docker Image'){
            steps{
                sh '''
                echo $enableVersion
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
    def source_code_hash  = "nRC9RyWtg2Mh9xUCG+vt9F+"
    def old_source_code_hash = null
    if (old_source_code_hash == source_code_hash)
    return true
    else
    return false
    def old_source_code_hash = source_code_hash
}
