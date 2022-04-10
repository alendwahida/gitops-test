pipeline {
    agent any
    stages {
        stage('Update Image Version Deployment K8s') {
            steps {
                sh "ls"
                sh "cat gitops-test/staging/deployment.yaml"
                sh "sed -i 's+alendwahida/gitops-test. *+alendwahida/gitops-test:$IMAGE_TAG+g' gitops-test/staging/deployment.yaml"
                sh "cat staging/deployment.yaml"
            }
        }
    }
}
