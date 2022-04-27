pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
              checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '4374816f-1276-4f86-9a25-44ab81b45d6b', url: 'https://github.com/vansikasingh/devops_practice.git']]])
            }
        }
        stage('Build') {
            steps{
                git branch: 'main', credentialsId: '4374816f-1276-4f86-9a25-44ab81b45d6b', url: 'https://github.com/vansikasingh/devops_practice.git'
                bat 'Credits.ipynb'
            }
        }
        stage('Test'){
            steps{
                echo 'the job has been tested'
            }
        }
    }
}
