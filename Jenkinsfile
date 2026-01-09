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
	stages{
		stage('clone'){
			steps{
				git branch: 'feature_1', credentialsId: 'docker-jenkin', url: 'https://github.com/ngockien4102/t3h__devOps'
			}
		}

		stage('Docker') {
			steps{
				withDockerRegistry(credentialsId:'ngockien0410', url:''){
					sh label: '', script: 'docker build -t ngockien/testJenkin .'
					sh label: '', script: 'docker push ngockien/testJenkin'
				}
			}
		}
	}
}