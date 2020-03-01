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
				// deleteDir()

				echo "the build number is ${currentBuild.number}"
				echo 'Cleanup Done'
			}
		}
		
		stage('CheckOut latest Code')
		{
			steps
			{
				// checkout scm
				sh """
					ls -ltr
				"""
			}
		}
		stage('did the changes')
		{
			steps
			{
				sh """
					git config --global user.name "learn-cloud"
    					git config --global user.email githubanand@gmail.com
					ls -ltr
					git checkout -b anand_test
					echo "new line" >> index.html
					git status
					git add index.html
					git status
					git commit -m "test anand"
					git push --set-upstream origin anand_test
					
				"""
				
			}
		}
	}
}
