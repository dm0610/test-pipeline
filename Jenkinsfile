pipeline {
    agent any
    environment {
        YAMLS = 'https://github.com/dm0610/kube-labs.git'
    } 
    stages {
        stage('Deliver for master') {
            when {
                branch 'master' 
            }
            steps {
                git([url: 'https://github.com/dm0610/kube-labs.git', branch: 'master', credentialsId: '	d90e03eb-0141-4f18-ba1d-973736a8febd'])
                sh './shell/test.sh'
            }
        }
        stage('Deploy for second') {
            when {
                branch 'second-branch'  
            }
            steps {
                git([url: 'https://github.com/dm0610/kube-labs.git', branch: 'second-branch', credentialsId: '	d90e03eb-0141-4f18-ba1d-973736a8febd'])
                sh './shell/test.sh'
            }
        }
        stage('Deploy for third') {
            when {
                branch 'third-branch'  
            }
            steps {
                git([url: 'https://github.com/dm0610/kube-labs.git', branch: 'third-branch', credentialsId: '	d90e03eb-0141-4f18-ba1d-973736a8febd'])
                sh './shell/test.sh'
            }
        }
    }
}
