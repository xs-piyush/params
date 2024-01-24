pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'kubectl config --kubeconfig=/var/lib/jenkins/.kube/config view'
                sh '/snap/bin/kubectl get po'
            }
        }
    }
}
