pipeline {
    agent any
    stages {
        stage('Update Image Version Deployment K8s') {
            steps {
                sh "git config user.email alendwahida@gmail.com"
                sh "git config user.name alendwahida"
                sh "ls"
                sh "printenv"
                sh "cat staging/deployment.yaml"
                sh "sed -i 's+com/sosialmedia. *+com/sosialmedia:$IMAGE_TAG+g' staging/deployment.yaml"
                sh "cat staging/deployment.yaml"
                sh "git add ."
                sh "git commit -m '$IMAGE_TAG'"
                sh "git tag '$IMAGE_TAG'"
                sh "git status"
                sh "git push https://$GIT_TOKEN@github.com/alendwahida/gitops-test.git HEAD:main"
            }
        }
    }
}
