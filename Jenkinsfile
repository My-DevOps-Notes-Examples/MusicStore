pipeline {
    agent { label 'Dotnet6' }
    triggers { pollSCM('* * * * *')}
    stages {
        stage('VCS') {
            steps {
                git url: 'https://github.com/My-DevOps-Notes-Examples/MusicStore.git',
                branch: 'declarative'
            }
        }
        stage('Build') {
            steps {
                sh 'dotnet restore ./MusicStore/MusicStore.csproj && dotnet build ./MusicStore/MusicStore.csproj'
            }
        }
    }
}