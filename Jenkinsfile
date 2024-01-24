pipeline {
    agent any
    stages {
        stage('build') {
            steps {
              sh "sed 's/url/url1/' be.yaml"
              sh "cat be.yaml"
            }
        }
    }
}
