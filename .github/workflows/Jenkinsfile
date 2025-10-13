pipeline {
    agent any
    stages { 
        stage('Restore Project dependences') {
            steps {
                sh 'dotnet restore'
            }
        }
        stage('Build Project') {
            steps {
                sh 'dotnet build --no-restore'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}