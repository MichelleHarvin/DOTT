pipeline {
    agent any


    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
     
        stage('SonarQube analysis') {
            steps { withSonarQubeEnv(installationName:'sonar')
                   withMaven (maven:'mvn'){
                sh 'mvn verify org.sonarsource.scanner.maven:sonar-maven-plugin:sonar -Dsonar.projectKey=MichelleHarvin_DOTT'}   
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
