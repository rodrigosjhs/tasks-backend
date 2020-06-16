pipeline{
    agent any
    stages{
        stage("Build Backend"){
            steps{
                bat 'mvn clean package -DskipTests=true'
            }
        }
        stage("Unit Tests"){
            steps{
                bat 'mvn test'
            }
        }
        stage("Sonar Analysis"){
            steps{
                bat "C:\Users\"Rodrigo Pereira"\.jenkins\tools\hudson.plugins.sonar.SonarRunnerInstallation\SONAR_SCANNER\bin/sonar-scanner -e -Dsonar.projectKey=DeployBack -Dsonar.host.url=http://localhost:9000 -Dsonar.login=751c7ee18731988a6b6ffe8a357f9f667823d913 -Dsonar.java.binaries=target"
            }
        }        
    }
}


