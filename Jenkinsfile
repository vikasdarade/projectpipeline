pipeline{
	agent{
		label{
			label "built-in"
			customWorkspace "/home/ansible/project1"
		}
	}
	environment{
	PATH ="/mnt/devtool/apache-maven-3.8.6/bin:$PATH"
	}
	stages{
		stage('git clone code'){
			steps{
			sh "sudo rm -rf *"
			git 'https://github.com/vikasdarade/projectpipeline.git'
				
			}
		}
		stage ('code build') {
			steps{
				sh "mvn install"
			}
		}

	}
}
