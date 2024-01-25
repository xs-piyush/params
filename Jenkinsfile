pipeline {
    agent any
    stages {
        stage('Function') {
            steps {
                script {
                    echo "Building for distribution: ${params.imageurl}"
                    sh "sed -e 's/name: utn/name: ${params.name}/g' -e 's/image: atu/image: ${params.imageurl}/g' be.yaml > bf.yaml"
      //              sh "sed 's/name: utn/name: ${params.name}/g' be.txt > bf.txt"
     //               sh "cat bf.txt"
    //                sh "sed 's/name: atn/name: ${params.imageurl}/g' be.txt > bf.txt"
                    sh "cat bf.yaml"
                    sh "rm -f bf.yaml"
                }
            }
        }
        stage('Choose') {
            steps {
                sh "cat bf.yaml"
            }
        }
    }
}
