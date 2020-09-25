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
				sshagent(['sshroot-1']) {
					sh 'ssh -o StrictHostKeyChecking=no -l root 209.182.237.42 touch test1.txt'
				}
            }
        }
   }
}