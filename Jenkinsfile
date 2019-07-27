pipeline {
    agent {
        any
        }
    }
    environment {
        YAMLS = 'https://github.com/dm0610/kube-labs.git'
    }
        stage('Then branch is master') {
            when {
                branch 'master' 
            }
            steps {
                git([url: $YAMLS, branch: 'master', credentialsId: 'd90e03eb-0141-4f18-ba1d-973736a8febd'])
                sh './shell/test.sh'
            }
        }
        stage('Then branch is second') {
            when {
                branch 'second-branch'  
            }
            steps {
                git([url: $YAMLS, branch: 'master', credentialsId: 'd90e03eb-0141-4f18-ba1d-973736a8febd'])
                sh './shell/test.sh'
            }
        }
        stage('Then branch is third') {
            when {
                branch 'third-branch'  
            }
            steps {
                git([url: $YAMLS, branch: 'master', credentialsId: 'd90e03eb-0141-4f18-ba1d-973736a8febd'])
                sh './shell/test.sh'
            }
        }
    }
}
