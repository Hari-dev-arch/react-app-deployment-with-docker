pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('changing the file permission') {
            steps {
                sh 'chmod +x build.sh'
            }
        }

        stage('executing the file') {
            steps {
                sh './build.sh'
            }
        }
    }
}
