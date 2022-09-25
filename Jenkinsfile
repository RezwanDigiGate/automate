pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
    }

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git credentialsId: 'git-credential', url: 'https://github.com/RezwanDigiGate/automate.git'
            }
        }
        stage("maven compile"){
            steps{
                bat script: "mvn compile"
            }
        }
        stage("maven build"){
            steps{
                bat script: "mvn test"
            }
        }
    }
}
