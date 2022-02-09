pipeline {
    agent {
        node {
            label 'slave1'
        }
    }
    stages {
        stage('Disk Usage') {
            steps {
                sh 'df -Tk'
            }
        }
        stage('System Info') {
            steps {
                sh 'uname -a'
                sh 'date'
                sh 'pwd'
            }
        }
        stage('Find non accessible files') {
            steps {
                sh 'find / -ls 1>/dev/null || true'
            }
        }
        stage('ENV') {
            steps {
                sh 'env'
                sh 'export'
            }
        }
    }
}