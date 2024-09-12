pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: 'main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Gayu9105/apache-log-parser-python.git']]])
            }
        }
        stage('Build') {
            steps {
                git branch: 'main', url: 'hhttps://github.com/Gayu9105/apache-log-parser-python.git'
                sh 'apache-log-parser.py'
            }
        }
        stage('Test') {
            steps {
                sh 'python3 -m pytest'
            }
        }
    }
}
