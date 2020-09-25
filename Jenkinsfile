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
					sh 'ssh -o StrictHostKeyChecking=no -l root 209.182.237.42 touch test1.txt'
				}
            }
        }
   }
}