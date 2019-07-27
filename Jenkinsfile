pipeline {
    agent any
    
    stages {
        stage('get Path') {
            steps {
                sh "pwd"
            }
        }
        stage('Copy') {
            steps {
                git url: 'https://github.com/dm0610/kube-labs.git'
            }
        }
        stage('Build') {
            steps {
                kubernetesDeploy configs: 'deploy-nginx/*', kubeconfigId: 'kubeconfig'
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
