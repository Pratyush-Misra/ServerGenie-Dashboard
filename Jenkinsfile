@Library('github.com/releaseworks/jenkinslib') _

pipeline {
    agent any
    stages {
        stage('submit stack') {
            steps {
                withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'aws-key', usernameVariable: 'AWS_ACCESS_KEY_ID', passwordVariable: 'AWS_SECRET_ACCESS_KEY']]) {
                    AWS("cloudformation create-stack --stack-name my-vpc-jenkins --template-body file://template.yml --region ap-south-1")
                }
            }
        }
    }
}