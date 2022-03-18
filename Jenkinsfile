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
                withSonarQubeEnv(installationName:'sonar') 
                mvn verify org.sonarsource.scanner.maven:sonar-maven-plugin:sonar-maven-plugin:3.6.0.projectKey=MichelleHarvin_DOTT
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        
        
         stage('Unit testing') {
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
