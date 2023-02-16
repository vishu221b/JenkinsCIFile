pipeline {
    agency any
        stages {
            stage('Test CMD'){
                steps('OUTPUT'){
                    sh 'pwd'
                    sh 'ls -al'
                    sh 'docker container ls'
                    sh 'docker image ls'
                }
            }
            agent {
                docker { image 'node:16.13.1-alpine' }
            }
            stage('Test') {
                steps {
                    sh 'node --version'
                }
            }
    }
    post { 
        always { 
            cleanWs()
        }
    }
}
