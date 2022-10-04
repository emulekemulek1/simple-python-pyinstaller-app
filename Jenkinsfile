pipeline {
    agent none
    environment {
     PATH = "/bin:/usr/bin:usr/local/bin"
    }
    stages {
        stage('Build') { 
            agent {
                docker {
                    image 'python:2-alpine' 
                    args "-u root"
                }
            }
            steps {
                sh 'echo gowno'
                // sh 'python -m py_compile sources/add2vals.py sources/calc.py' 
                // stash(name: 'compiled-results', includes: 'sources/*.py*') 
            }
        }
    }
}

