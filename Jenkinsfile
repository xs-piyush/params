pipeline {
    agent any
    stages {
        stage('Function') {
            steps {
                script {
                    echo "Building for distribution: ${params.imageurl}"
                    sh "sed 's/name: nginx-deployment/name: ${params.name}/g' be.txt"
                    sh "sed 's/image: nginx/image: ${params.imageurl}/g' be.txt"
                    sh "cat be.txt"
                    sh "rm -f be.txt"
                }
            }
        }
        stage('Choose') {
            steps {
                sh "echo 'hello'"
            }
        }
    }
}
