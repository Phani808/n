pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
      kubernetesDeploy configs: 'deployment.yml','service.yml,
          kubeconfigId: 'kubeconfig'
            }
        }
    }
}
