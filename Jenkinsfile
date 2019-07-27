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
                git([url: $YAMLS, branch: 'master'])
                sh './shell/test.sh'
            }
        }
        stage('Then branch is second') {
            when {
                branch 'second'  
            }
            steps {
                git([url: $YAMLS, branch: 'second'])
                sh './shell/test.sh'
            }
        }
        stage('Then branch is third') {
            when {
                branch 'third'  
            }
            steps {
                git([url: $YAMLS, branch: 'third'])
                sh './shell/test.sh'
            }
        }
    }
}
