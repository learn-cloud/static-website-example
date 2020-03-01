#!/groovy
def dockerImageRepo = 'gatewaytech/gatewaytech-ui'
def dockerImageTag
def dockerImage
def dockerRegistry = 'hub.docker.com'
def branchToUse = env.BRANCH

pipeline
{
	agent any
	stages
	{
		stage('Cleaning the WorkSpace')
		{
			steps
			{
				deleteDir()
				echo "the build number is ${currentBuild.number}"
				echo 'Cleanup Done'
			}
		}
		
		stage('CheckOut latest Code')
		{
			steps
			{
				checkout scm
			}
		}
		stage('did the changes')
		{
			steps
			{
				sh """
					ls -ltr
				"""
				
			}
		}
	}
}
