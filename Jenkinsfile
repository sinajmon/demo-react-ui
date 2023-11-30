pipeline {
    agent any

    stages {
        stage('Copy file to S3 bucket') {
            steps {
                withAWS(region: 'us-east-1', credentials: 'aws-jenkins-demo') {
                    sh "aws s3 cp ${source_file_path} s3://${s3_bucket_name}/"
                }
            }
        }
    }
}