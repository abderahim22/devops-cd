pipline
{
	agent any 

	stages {
		stage('Pull') {
		steps{
			scripts{
				chekout([$class:  'GitSCM', branches: [[name: '*/master']],
			userRemoteConfigs: [[
			credentialsId: 'GitHubCredentialsForJenkins'
			url: 'https://github.com/abderahim22/devops-cd.git']]
			])
		}
	}
}
