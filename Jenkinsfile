pipeline{
	agent {
		label{
			label "dev"
			customWorkspace "/home/ansible/project1"
		}
	}
	stages {
		stage ('git clone'){
			step {
			git branch: 'devops', url: 'https://github.com/vikasdarade/projectpipeline.git'
			}
		}
		stage ('run ansible playbook') {
			step {
			ansiblePlaybook credentialsId: 'ansible', disableHostKeyChecking: true, installation: 'ansible', inventory: 'host.inv', playbook: 'ansible-playbook.yaml'
			}
		}
	}
}
