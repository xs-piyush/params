pipeline {
    agent any
    stages {
        stage('Function') {
            steps {
                script {
                    echo "Building for distribution: ${params.imageurl}"
                    sh "sed 's/name: utn/name: ${params.name}/g' be.txt > bf.txt"
                    sh "cat bf.txt"
                    sh "sed 's/name: atn/name: ${params.imageurl}/g' be.txt > bf.txt"
                    sh "cat bf.txt"
                    sh "rm -f bf.txt"
                }
            }
        }
        stage('Choose') {
            steps {
                sh "cat bf.txt"
            }
        }
    }
}
