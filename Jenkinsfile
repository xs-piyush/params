pipeline {
    agent any
    stages {
        stage('Function') {
            steps {
                script {
                    echo "Building for distribution: ${params.imageurl}"
                    sh "sed 's/utn/${params.name}/' be.txt > bf.txt"
                    sh "sed 's/atn/${params.imageurl}/' be.txt > bf.txt"
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
