pipeline{
	agent any 
	stages {
		stage ('Build'){
			steps {
				echo "Building stage"
			}
		}
		stage ('Test'){
			steps {
				echo "Testing stage"
			}
		}
		stage ('Deploy to S3'){
			steps{
				echo "Deploying"
				withAWS(credentials: 'aws-credentials', region: 'us-east-1') {
				sh 'aws s3 cp ./index.html s3://mupreti.com.np'
				}
			}
		}
		}
	}
	
