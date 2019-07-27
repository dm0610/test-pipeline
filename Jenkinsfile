pipeline {
    agent any
    environment {
        YAMLS = 'https://github.com/dm0610/kube-labs.git'
    } 
    stages {
        stage('Deliver for development') {
            when {
                branch 'master' 
            }
            steps {
                git([url: https://github.com/dm0610/kube-labs.git, branch: 'master'])
                sh './shell/test.sh'
            }
        }
        stage('Deploy for production') {
            when {
                branch 'second'  
            }
            steps {
                git([url: https://github.com/dm0610/kube-labs.git, branch: 'second'])
                sh './shell/test.sh'
            }
        }
        stage('Deploy for production') {
            when {
                branch 'third'  
            }
            steps {
                git([url: https://github.com/dm0610/kube-labs.git, branch: 'third'])
                sh './shell/test.sh'
            }
        }
    }
}
