


pipeline {
    agent any
	
    stages {
        stage('Upload to S3') {
            steps {
                withAWS(region: 'us-east-1', credentials: 'jenkins-s3-credentials') {
                    s3Upload(
                        file: 'index.html',
                        bucket: 'my-s3-bucket',
                        path: 'some/path/in/bucket'
                    )
                }
            }
        }
    }
}
