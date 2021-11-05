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
                  //bat label: '', script: "minikube start --nodes 2 -p kube-node"
                  //bat label: '', script: "kubectl get nodes"
                  //sh label: '', script: 'pwd'
                  sh label: '', script: 'kubectl get nodes'
                  bat label: '', script: 'kubectl get nodes'              
                }                                  
            }
        }
        stage('Deploy-Hello-World_Container')
        {
            steps
            {
                dir('C:\\tmp\\DevOps-Automation-Challenge') {
                  bat label: '', script: "kubectl apply -f hello-world-deployment.yaml" 
                  bat label: '', script: "kubectl get deployments"
                  bat label: '', script: "kubectl get pods -o wide"
                  bat label: '', script: "kubectl get replicasets"             
                }  

            }
        }
        stage('Deploy-Ingress')
        {
            steps
            {
                dir('C:\\tmp\\DevOps-Automation-Challenge') {
                  bat label: '', script: "minikube addons enable ingress"
                  bat label: '', script: "kubectl apply -f hello-world-ingress.yaml"
                  bat label: '', script: "kubectl get ingress"              
                }  
            }
        }
              
    }
}