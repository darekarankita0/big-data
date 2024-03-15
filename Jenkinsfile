pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                git branch: 'main', url: 'https://github.com/vastevenson/pytest-intro-vs.git'
                sh 'python3 build.py'
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
