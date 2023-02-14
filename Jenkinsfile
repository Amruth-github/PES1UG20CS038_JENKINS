pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ PES1UG20CS038.cpp -o PES1UG20CS038'
                build job: 'PES1UG20CS038-1'
            }
        }
        
        stage('Test') {
            steps {
                sh './PES1UG20CS038'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deployment'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
