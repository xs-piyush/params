pipeline {
    agent any
    stages {
        stage('Function') {
            steps {
                script {
                    echo "Building for distribution: ${params.imageurl}"
                    sh "sed -e 's/name: utn/name: ${params.name}/g' -e 's/image: atu/image: ${params.imageurl}/g' be.yaml > bf.yaml"
                    sh "kubectl apply -f bf.yaml"
                    sh "rm -f bf.yaml"
                }
            }
        }
        stage('Choose') {
            steps {
                sh "Kubectl get po"
            }
        }
    }
}
