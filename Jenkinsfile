pipeline {
    agent any
    
    stages {
        stage('get Path') {
            steps {
                sh "pwd"
            }
    stages {
        stage('Copy') {
            steps {
                git url: 'git@github.com:dm0610/kube-labs.git'
            }
        }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
