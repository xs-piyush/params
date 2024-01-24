pipeline {
    agent any
 
    stages {
        stage('Function') {
            steps {
                script {
                    def value1
                    def value2
 
                    if (params.image == 'Image=nginx:latest, Deployment Name: Nginx-deployment') {
                        value1 = 'params.${Enter_Name_of_your_Deployment}'
                        value2 = 'params.${Enter_Url_of_you_Image}'
                    } else if (params.image == 'Image=httpd, Deployment Name: Apache-deployment') {
                        value1 = 'params.$Enter_Name_of_your_Deployment'
                        value2 = 'params.$Enter_Url_of_you_Image'
                    }
 
                    echo "Building for distribution: ${params.image}"
 
                    sh "sed 's/utn/${value2}/g' be.yaml > bf.yaml"
                    sh "sed 's/atn/${value1}/g' be.yaml > bf.yaml"

                }
            }
        }
 
        stage('Choose') {
            steps {
                    sh "cat bf.yaml"
                    sh "rm -f bf.yaml"
            }
        }
    }
}
