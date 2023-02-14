pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ PES1UG20CS038.cpp'
                build job: 'PES1UG20CS038-1'
            }
        }
        
        stage('Test') {
            steps {
                sh './a.out'
            }
        }
        
        stage('Deploy') {
            steps {
                eco 'Deployment'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
