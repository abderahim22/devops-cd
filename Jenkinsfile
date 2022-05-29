pipeline
{
	agent any 
	stages {
		stage('Pull') {
			steps{
				script{
					chekout([$class:  'GitSCM', branches: [[name: '*/master']],
				userRemoteConfigs: [[
					credentialsId: 'GitHubCredentialsForJenkins',
					url: 'https://github.com/abderahim22/devops-cd.git']]
				])}
			}
		}
	}
}
