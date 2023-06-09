pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                kubernetesDeploy configs: 'deployment.yml,service.yml',
                    kubeconfigId: 'kubeconfig'
            }
        }

        stage('Run Ansible Playbook') {
  steps {
    ansiblePlaybook becomeUser: 'jenkins',
                   colorized: true,
                   credentialsId: 'jenkins-slave',
                   installation: 'Ansible',
                   inventory: './hosts',
                   playbook: '/home/mpvarma997/playbook.yml'
  }
}
    }
}
