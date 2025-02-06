pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git credentialsId: 'Jenkins-GitHub-Integration', url: 'https://github.com/aravind-zinnect/automatePipeline', branch: 'main'
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
