pipeline {
  agent any
  stages {    
    
    stage('Checkout external proj') {
        steps {
            git branch: 'master',
                credentialsId: '922aa409-e2fd-4bc9-bb8d-47204bfc9cd7',
                url: 'https://github.com/dburcombe/python_project_demo.git'

            
        }
    }
  
    stage('Build') {

        steps {
                ls -lrt
                pwd
                sh 'python3 operations.py' 
        }
    }


    }
}
