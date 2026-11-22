
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
                bat 'if not exist index.html exit /b 1'
                echo 'HTML file exists'
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

}
