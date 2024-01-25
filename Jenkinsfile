pipeline {
    agent any
    stages {
        stage('Function') {
            steps {
                script {
                    echo "Building for distribution: ${params.imageurl}"
                    sh "sed 's/name: utn/name: ${params.name}/' be.txt > bf.txt"
                    sh "sed 's/image: atn/image: ${params.imageurl}/' be.txt > bf.txt"
                    sh "cat bf.txt"
                    sh "rm -f bf.txt"
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
