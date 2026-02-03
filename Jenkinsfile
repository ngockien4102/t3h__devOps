//pipeline{
//	agent any
//	stages{
//		stage('Clone'){
//			steps{
//				echo 'start clone'
//				git branch: 'feature_1', url: 'https://github.com/ngockien4102/t3h__devOps.git'
//				echo 'done clone'
//			}
//		}
//
//		stage('Build'){
//			steps{
//				echo 'build code'
//			}
//		}
//
//		stage('Test'){
//			steps{
//				echo 'run unittest'
//			}
//		}
//
//		stage('Docker'){
//			steps{
//				echo 'build image'
//				echo 'tag'
//				echo 'push docker hub'
//			}
//		}
//	}
//}

pipeline{
	agent any
	stages{
		stage('clone'){
			steps{
				git branch: 'feature_1', credentialsId: 'github-jenkins', url: 'https://github.com/ngockien4102/t3h__devOps'
			}
		}

		stage('Docker') {
			steps{
				withDockerRegistry(credentialsId:'jenkin_token', url:''){
					sh label: '', script: 'docker build -t ngockien0410/testJenkin .'
					sh label: '', script: 'docker push ngockien0410/testJenkin'
				}
			}
		}
	}
}