

pipeline {
    agent any
    stages {
        stage('Copy file from git to AWS S3 bucket') { 
            steps {
               withAWS(region: 'us-east-1', credentials: 'aws-jenkins-demo') {
                   sh 'aws s3 cp Code/index.html s3://jenkin-s3'
               }
            }
        }
    }
}