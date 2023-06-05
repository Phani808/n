pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
              kubernetesDeploy configs: '', enableConfigSubstitution: false, kubeConfig: [path: 'deployment.yml'], kubeconfigId: 'kubeconfig', secretName: '', ssh: [sshCredentialsId: '*', sshServer: ''], textCredentials: [certificateAuthorityData: '', clientCertificateData: '', clientKeyData: '', serverUrl: 'https://']
               sh 'kubectl get pods'
            }
        }
    }
}
