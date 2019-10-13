pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'mvn pacakage'
            }
        }
        
        stage('SonarQube analysis') { 
        withSonarQubeEnv('Sonar') { 
          sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.3.0.603:sonar'
        }
        }
    }
}
