pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                git branch: 'test', url: 'https://github.com/darekarankita0/big-data.git'
                sh 'python3 jenkinstest.py'

            }
        }


         stage('Package') {
            steps {
               sh 'zip -r jenkinsproj.zip .'
            }
        }
        
        stage('Deploy') {
            steps {
               echo 'deploy'
            }
        }
	
    }
}
