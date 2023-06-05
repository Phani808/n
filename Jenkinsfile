pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
               kubernetesDeploy configs: 'deployment.yml', kubeconfigId: 'kubeconfig')
               sh 'kubectl get pods'
            }
        }
    }
}
