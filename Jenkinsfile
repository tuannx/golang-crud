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
				sh 'docker-compose up -d'
            }
        }
   }
}