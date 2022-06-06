pipeline
{
	agent any 
	stages {
		stage('Pull') {
			steps{
				script{
					checkout([$class:  'GitSCM', branches: [[name: '*/master']],
				userRemoteConfigs: [[
					credentialsId: 'GitHubCredentialsForJenkins',
					url: 'https://github.com/abderahim22/devops-cd.git']]
				])}
			}
		
		}
		
		
		
 stage('Install')
 
 { 
 
        steps {
        
        script{
        sh  "npm install"
        
                           }
        
                      }
        
                 }
		

 stage('Build')
 
 { 
 
        steps {
        
        script{
        sh  "ansible-playbook ansible/build.yml  -i ansible/inventory/host.yml"
        
                           }
        
                      }
        
                 }
           stage('docker')
 
 { 
 
        steps {
        
        script{
        sh  "ansible-playbook ansible/docker.yml  -i ansible/inventory/host.yml"
        
                           }
        
                      }
        
                 }
	}
}
