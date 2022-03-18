pipeline {
    agent any


    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
     
        stage('SonarQube analysis') {
            def scannerHome = tool 'SonarScanner 4.0';
            withSonarQubeEnv(installationName:'sonar') {
                withMaven (maven:'mvn')
                {mvn clean verify sonar:sonar
                mvn clean install
                 mvn sonar:sonar
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
