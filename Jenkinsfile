pipeline{
	agent any
	tools{
		gradle 'Gradle'
		jdk 'Jdk'
	}
	stages{
		stage('Checkout'){
			steps{
			git branch: 'main', url:'https://github.com/Gurukiran-H-S/2023GradleApp.git'
			}
		}
		stage('Build'){
			steps{
				sh 'gradle test'
				}
			}
		stage('Run Application'){
			step{
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
