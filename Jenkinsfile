pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                withCredentials([string(credentialsId: 'kubeconfig-local', variable: 'kube-local')]) {
                sh 'kubectl config --kubeconfig=/var/lib/jenkins/.kube/config view'
                sh '/snap/bin/kubectl get po'
                }
            }
        }
    }
}
