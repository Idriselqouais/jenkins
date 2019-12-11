pipeline {
	agent any
	tools {
		maven 'Maven 3'
		jdk 'jdk1.8.0_191'
	}
        satges{
             stage('Build'){

             	steps{
             		bat 'mvn install'
             	}
             	post{
             		success {
             			junit 'target/surefire-report/**/*.xml'
             		}
             	}
               }
}
}