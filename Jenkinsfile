pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
    }

    post {
        success {
            mail to: 'dumiferdinands@gmail.com',
                 subject: "SUCCESS: ${env.JOB_NAME} Build #${env.BUILD_NUMBER}",
                 body: "Good news 🎉\n\nThe build succeeded!\nCheck details: ${env.BUILD_URL}"
        }
        failure {
            mail to: 'dumiferdinands@gmail.com',
                 subject: "FAILED: ${env.JOB_NAME} Build #${env.BUILD_NUMBER}",
                 body: "Uh oh 🚨\n\nThe build failed!\nCheck logs: ${env.BUILD_URL}"
        }
    }
}
