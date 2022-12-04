node() {
    
    stage('clone git project') {
        git branch: 'main', url: 'https://github.com/akulabharath01/K8S_01Oct22.git'
    }
    
    stage('getnodes') {
        withKubeConfig([credentialsId: 'kubernetes-config']) {
        sh 'curl -LO "https://storage.googleapis.com/kubernetes-release/release/v1.20.5/bin/linux/amd64/kubectl"'  
        sh 'chmod u+x ./kubectl'  
        sh './kubectl get nodes'
    }

    }
    
    stage('deploy') {
        
        sh 'kubectl apply -f deployment.yml'
        sh 'kubectl apply -f javaappservice.yml'
        
    }
}
