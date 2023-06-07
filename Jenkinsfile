pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                kubernetesDeploy configs: 'deployment.yml,service.yml',
                    kubeconfigId: 'kubeconfig'
            }
        }

        stage('Deploy') {
            steps {
                sh 'ansible-playbook -i hosts playbook.yml'
            }
        }
    }
}
