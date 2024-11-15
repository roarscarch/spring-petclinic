pipeline {
    agent any

    stages {
        stage('Initialize') {
            steps {
                echo 'Starting the build process...'
            }
        }
        stage('Build WAR') {
            steps {
                echo 'Building WAR file...'
                sh './mvnw clean package' // Builds the WAR file
            }
        }
        stage('Archive WAR') {
            steps {
                echo 'Archiving WAR file...'
                archiveArtifacts artifacts: 'target/*.war', fingerprint: true
            }
        }
    }
}
