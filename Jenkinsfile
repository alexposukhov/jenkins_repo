pipeline {
    agent any

    stages {
        stage('Build W/O Docker') {
            steps {
                echo 'Building project without docker'
            }
        }
        stage('Build With Docker') {
            agent {
                docker {
                    image 'ubuntu:20.04'
                    reuseNode true
                }
            }
            steps {
                echo 'Building project with docker'
                sh '''
                    uname -a
                    cat /etc/os-release
                '''    
            }
        }
    }
}