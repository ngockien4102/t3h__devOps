pipeline{
	agent any
	stages{
		stage('Clone'){
			steps{
				echo 'clone'
			}
		}

		stage('Build'){
			steps{
				echo 'build code'
			}
		}

		stage('Test'){
			steps{
				echo 'run unittest'
			}
		}

		stage('Docker'){
			steps{
				echo 'build image'
				echo 'tag'
				echo 'push docker hub'
			}
		}
	}
}