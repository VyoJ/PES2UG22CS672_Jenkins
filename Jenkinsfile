pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ main.cpp -o output'
                build 'PES2UG22CS672-1'
            }
        }
        stage('Test') {
            steps {
                sh './output'
                echo 'Test successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }
    post {
        success {
            echo 'Pipeline successful'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}