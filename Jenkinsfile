pipeline {
    agent any

    environment {
        LABS = credentials('labcreds')
    }

    stages {
        stage('Build') {
            steps {
               sh 'pip3 install --user pipenv'
               sh '/bitnami/jenkins/home/.local/bin/pipenv --rm || exit 0'
               sh '/bitnami/jenkins/home/.local/bin/pipenv install'
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
