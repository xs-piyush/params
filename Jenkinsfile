pipeline {
    agent any
    stages {
        stage('Function') {
            steps {
                script {
                    echo "Building for distribution: ${params.imageurl}"
                    sh "sed 's/name: utn/name: ${params.name}/g' be.txt"
                    sh "sed 's/image: atn/image: ${params.imageurl}/g' be.txt"
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
