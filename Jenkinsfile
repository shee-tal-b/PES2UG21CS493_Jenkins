pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo  'build'
                    sh 'g++ main.cpp -o output'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    echo 'test'
                    sh './output'  
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    echo 'deploy'
                }
            }
        }
    }

    post {
        failure {
            echo 'pipeline failed'
        }
    }
}
