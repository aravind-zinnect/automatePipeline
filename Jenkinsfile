pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/your-username/Jenkins-GitHub-Windows.git'
            }
        }
        stage('Run Script') {
            steps {
                bat 'script.bat' // Change this to 'sh script.sh' if using Linux
            }
        }
        stage('Archive Output') {
            steps {
                archiveArtifacts artifacts: '**/*.txt', fingerprint: true
            }
        }
    }
}
