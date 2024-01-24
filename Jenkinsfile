pipeline {
    agent any
    stages {
        stage('function')
           steps {
             script {
                   def value1
                   def value2
                   if (params.image-and-name == 'nginx:latest') {
                        value1 = 'nginx:latest'
                        value2= 'Nginx-deployment'
                    } else if (params.image-and-name == 'httpd:latest') {
                        value = 'httpd:latest'
                        value2= 'Apache-deployment'
                    }
                    
                    echo "Building for distribution: ${params.image-and-name}"
                    sh "sed 's/utn/$value2/' be.yaml > bf.yaml"
                    sh "sed 's/atn/$value1/' be.yaml > bf.yaml"
                    sh "cat bf.yaml"
                    sh "rm -f bf.yaml"
                }
            }
    
      stages {
        stage('Choose') {
            steps {
              sh "echo "hello"
             }
         }
     }
  }
}
