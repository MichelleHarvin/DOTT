pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
      stage('scan') {
            steps {
               withsonarQubeEnv(instalationName:'sq')
               {sh'./mvnw clean org.sonar}
            }
        }

        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Jaló...'
            }
        }
    }
}
