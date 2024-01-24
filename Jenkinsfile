pipeline {
    agent any
 
    stages {
        stage('Function') {
            steps {
                script {
                    def value1
                    def value2
 
                    if (params.image == 'nginx:latest') {
                        value1 = 'nginx:latest'
                        value2 = 'Nginx-deployment'
                    } else if (params.image == 'httpd:latest') {
                        value1 = 'httpd:latest'
                        value2 = 'Apache-deployment'
                    }
 
                    echo "Building for distribution: ${params.image}"
 
                    sh "sed 's/utn/${value2}/' bf.yaml > bf.yaml"
                    sh "sed 's/atn/${value1}/' bf.yaml > bf.yaml"
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
