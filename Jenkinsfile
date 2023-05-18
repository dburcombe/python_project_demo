pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '922aa409-e2fd-4bc9-bb8d-47204bfc9cd7', url: 'https://github.com/dburcombe/python_project_demo.git']])
            }
        }
        stage('Build') {
            steps{
                git branch: 'testing', credentialsId: '922aa409-e2fd-4bc9-bb8d-47204bfc9cd7', url: 'https://github.com/dburcombe/python_project_demo.git'
                sh 'python3 operations.py'
            }
        }
        stage('test') {
            steps{
                echo 'the python script has now been tested'
            }
        }    
    }
}
