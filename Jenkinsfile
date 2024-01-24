pipeline {
    agent any
    stages {
        stage('build') {
            steps {
              sh "sed 's/url/url1/' be.yaml > bf.yaml"
              sh "cat bf.yaml"
            }
        }
    }
}
