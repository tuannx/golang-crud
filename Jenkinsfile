pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/tuannx/golang-crud.git'
				sh 'pwd'
            }
        }
        stage('Build') {
            steps {
				withDockerRegistry(credentialsId: 'docker-hub', url: 'https://index.docker.io/v1/') {
					sh 'docker build -t tuannx/golang-crud:latest .'
					sh 'docker push -t tuannx/golang-crud:latest'
				}
            }
        }
       stage('Deploy') {
            steps {
				sshagent(['c622efd9-4b78-4fee-bcbe-1f9bc4f1b752']) {
					touch test.txt
				}
            }
        }
   }
}