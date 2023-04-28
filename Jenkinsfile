@Library('github.com/releaseworks/jenkinslib') _

pipeline {
    agent any
    stages {
        stage('submit stack') {
            steps {
                sh "aws cloudformation create-stack --stack-name my-vpc-2-jenkins --template-body file://template.yml --region ap-south-1"
            }
        }
    }
}