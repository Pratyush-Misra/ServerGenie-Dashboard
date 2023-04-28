pipeline {
    agent any
    stages {
        stage('submit stack') {
            steps {
                sh "aws cloudformation create-stack --stack-name my-vpc-jenkins --template-body file://template.yml --region ap-south-1"
            }
        }
    }
}