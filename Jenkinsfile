pipeline {
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/tuannx/golang-crud.git'
				sh 'pwd'
            }
        }
        stage('Clone') {
            steps {
				agent any
				// This step should not normally be used in your script. Consult the inline help for details.
				withDockerRegistry(url: 'https://index.docker.io/v1/') {
					sh 'docker build -t tuannx/golang-crud:latest .'
					sh 'docker push -t tuannx/golang-crud:latest'
					// some block
				}
            }
        }
    }
}