node() {
    
    stage('clone git project') {
        git branch: 'main', url: 'https://github.com/akulabharath01/K8S_01Oct22.git'
    }
    
    stage('deploy') {
        sh 'kubectl create -f deployment.yml'
        sh 'kubectl create -f .yml'
        
    }
}
