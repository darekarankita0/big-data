pipeline {
    agent any

    stages {

	stage('Install dependencies') {
            steps {
		echo 'install requirements.txt'

            }
        }
        stage('Build') {
            steps {
		echo 'py code'
                sh '/bitnami/jenkins/home/.local/bin.pipenv run build.py'

            }
        }
     stage('Test') {
            steps {
                git branch: 'feature-rp-1000', url: 'https://github.com/darekarankita0/big-data.git'
                sh 'python3 test.py'

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
