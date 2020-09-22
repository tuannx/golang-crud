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
				sh 'docker-composse up -d --build'
            }
        }
   }
}