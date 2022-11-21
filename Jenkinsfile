#node {
#	stage('Build') {
#		echo "Build for the second time 2"
#	}
#	stage('Test') {
#		echo "Test"
#	}
#}

//Declarative
pipeline{
	agent any
	stages{
		stage('Build'){
			steps {
					echo 'Building'
				}
			}
		stage('Test'){
			steps {
					echo 'Test'
				}
			}
	}
}