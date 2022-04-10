pipeline {
    agent any
    stages {
        stage('Update Image Version Deployment K8s') {
            steps {
                sh "ls"
                sh "printenv"
                sh "cat staging/deployment.yaml"
                sh "sed -i 's+com/sosialmedia. *+com/sosialmedia:$IMAGE_TAG+g' staging/deployment.yaml"
                sh "cat staging/deployment.yaml"
            }
        }
    }
}
