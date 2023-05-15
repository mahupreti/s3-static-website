pipeline{
	agent any 
	environment {
	AWS_DEFAULT_REGION = "us-east-1"
	THE_BUTLER_SAYS_SO = credentials('jenkins-aws')
	}
	stages {
		stage ('Build'){
			steps {
				echo "Building stage"
			}
		}
		stage ('Test'){
			steps {
				echo "Testing stage"
				sh ' aws ec2 describe-instances'
			}
		}
		
		}
	}
	
