pipeline{
	agent any
	tools{
		gradle 'Gradle'
		jdk 'JDK'
	}
	stages{
		stage('Checkout'){
			steps{
			git branch: 'main', url:'https://github.com/Gurukiran-H-S/GT.git'
			}
		}
		stage('Build'){
			steps{
				sh 'gradle test'
				}
			}
		stage('Run Application'){
			steps{
				sh 'gradle run'
			}
		}
	}
	post{
		success{
			echo 'Build and deployed successfully'
		}
		failure
		{
			echo 'Build failure'
		}
	}
}
