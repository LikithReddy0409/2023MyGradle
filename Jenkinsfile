pipeline{
	agent any
	tools{
		gradle 'Gradle'
		jdk 'JDK'
	}
	stages{
		stage('Checkout'){
			steps{
			git branch: 'main', url:'https://github.com/LikithReddy0409/2023MyGradle.git'
			}
		}
		stage('Build'){
			steps{
				sh 'gradle test'
				}
			}
		stage('Run Application'){
			steps{
				sh 'gradle display'
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
