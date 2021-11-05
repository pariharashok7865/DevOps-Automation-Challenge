pipeline 
{
    agent any
    stages 
    {
        stage('Deploy-Kube_Cluster')
        {
            steps
            {
                dir('C:\\tmp\\DevOps-Automation-Challenge') {
                    echo "inside dir block"
                    pwd()

            
                }  
                echo "outside dir block"
                pwd()
                
            }
        }
        stage('Deploy-Hello-World_Container')
        {
            steps
            {
                pwd()

            }
        }
        stage('Deploy-Ingress-Controller')
        {
            steps
            {
                pwd()
            }
        }
              
    }
}