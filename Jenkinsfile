pipeline {
    agent any

    enviroment{
    SCANNER_HOME= tool 'sonar'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
      stage('scan') {
            steps {
               withsonarQubeEnv('sonar')
               sh'mvn verify org.sonarsource.scanner.maven:sonar-maven-plugin:sonar -Dsonar.projectKey=MichelleHarvin_DOTT'
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
