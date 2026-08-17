pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building Java application...'
                sh 'mvn clean package -DskipTests'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Java application...'
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        success {
            echo 'Jenkins Pipeline SUCCESS!'
        }

        failure {
            echo 'Jenkins Pipeline FAILED!'
        }
    }
}
