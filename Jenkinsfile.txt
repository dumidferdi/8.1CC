pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                echo 'Hello from 8.2CDevSecOps'
            }
        }
    }
}
