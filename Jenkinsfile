//  node {
// 	stage('Build') {
// 		echo "Build for the second time 2"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// }

//Declarative
pipeline{
//	agent any
	agent { docker { maven '3.6.3'} }
	environment{
		dockerHome = tool 'docker'
		mavenHome = tool 'maven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages{
		stage('Build'){
			steps {
					sh 'mvn --version'
					sh 'docker version'
					echo 'Building for the testing'
				}
			}
		stage('Test'){
			steps {
					echo 'Test'
				}
			}
	}
	post{
		always{
			echo 'Executing always!'
		}
		success{
			echo 'I am running after success'
		}
		failure{
			echo 'I only run if any failure'
		}
		changed{
			echo ' i will execute if the build status is changed'
		}
	}
}