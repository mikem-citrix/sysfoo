pipeline {
	agent any
	
	tools {
		maven 'Maven 3.6.3'
	}
	
	stages {
		stage('build') {
			steps {
				echo 'Compile'
				sh 'mvn compile'
			}
		}
		stage('test') {
			steps {
				echo 'Test'
				sh 'mvn clean test'
			}
		}
		stage('package') {
			steps {
				echo 'Package'
				sh 'mvn package -DskipTests'
			}
		}
						
	}
}