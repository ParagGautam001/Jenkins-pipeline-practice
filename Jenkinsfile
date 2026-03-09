pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building application'
                sh 'echo Build successful > build.txt'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
                sh 'cat build.txt'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'build.txt'
            }
        }
    }
}
