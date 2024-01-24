pipeline {
    agent any
    stages {
        stage('build') {
            steps {
              sh "sed 's/nginx-deployment/url/' be.yaml"
            }
        }
    }
}
