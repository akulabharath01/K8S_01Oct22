node() {
    
    stage('clone git project') {
        git branch: 'main', url: 'https://github.com/akulabharath01/K8S_01Oct22.git'
    }
    
    stage('getnodes') {
        withKubeConfig(caCertificate: '', clusterName: '', contextName: '', credentialsId: '20e67df2-a3a9-4794-9d26-79622ce2caa8', namespace: '', serverUrl: '') {
    sh 'kubectl get nodes'
}

    }
    
    stage('deploy') {
        
        sh 'kubectl apply -f deployment.yml'
        sh 'kubectl apply -f javaappservice.yml'
        
    }
}
