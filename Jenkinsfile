pipeline {
    agent any
    stages {
        stage('Function') {
            steps {
                script {
                    echo "Building for distribution: ${params.imageurl}"
                    sh "sed 's/utn/${params.name}/' be.yaml > bf.yaml"
                    sh "sed 's/atn/${params.imageurl}/' be.yaml > bf.yaml"
                    sh "cat bf.yaml"
                    sh "rm -f bf.yaml"
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
