pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/tuannx/golang-crud.git'
				sh 'pwd'
            }
        }
        stage('Deploy') {
            steps {
				sshagent(['c622efd9-4b78-4fee-bcbe-1f9bc4f1b752']) {
					sh 'touch test.txt'
					sh 'docker-compose up -d'
				}
            }
        }
   }
}