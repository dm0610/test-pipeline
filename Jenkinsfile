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
                kubernetesDeploy configs: '', kubeConfig: [path: ''], kubeconfigId: 'kubeconfig', secretName: '', ssh: [sshCredentialsId: '*', sshServer: ''], textCredentials: [certificateAuthorityData: '', clientCertificateData: '', clientKeyData: '', serverUrl: 'https://']
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
