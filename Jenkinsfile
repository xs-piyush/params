pipeline {
    agent any
 
    stages {
        stage('Function') {
            steps {
                script {
                    if (params.image_and_name == 'Image=nginx:latest, Deployment Name: Nginx-deployment') {
                        sh "sed 's/utn/Nginx-deployment/' be.yaml > bf.yaml"
                        sh "sed 's/atn/nginx:latest/' be.yaml > bf.yaml"
                        sh "cat bf.yaml"
                        sh "rm -f bf.yaml"
                    } else if (params.image_and_name == 'Image=httpd, Deployment Name: Apache-deployment') {
                        sh "sed 's/utn/Apache-deployment/' be.yaml > bf.yaml"
                        sh "sed 's/atn/httpd:latest/' be.yaml > bf.yaml"
                        sh "cat bf.yaml"
                        sh "rm -f bf.yaml"                        
                    }
 
                    echo "Building for distribution: ${params.image_and_name}"
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
