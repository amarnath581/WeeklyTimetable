
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building Timetable'
            }
        }

        stage('Test') {
            steps {
                sh 'test -f index.html'
            }
        }

        stage('Deploy') {
            steps {
                archiveArtifacts 'index.html'
                echo 'Deployment Successful'
            }
        }
    }
}
