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
				step {
					echo 'Building'
				}
		}
			stage('Test'){
				step {
					echo 'Test'
				}
		}
}
