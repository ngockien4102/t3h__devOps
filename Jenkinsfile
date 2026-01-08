pipeline{
	agent any
	stages{
		stage('Clone'){
			steps{
				echo 'start clone'
				git branch: 'feature_1', url: 'https://github.com/ngockien4102/t3h__devOps.git'
				echo 'done clone'
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