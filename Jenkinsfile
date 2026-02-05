
pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build .NET Project') {
            steps {
                sh '''
                docker run --rm \
                  -v $PWD:/app \
                  -w /app \
                  mcr.microsoft.com/dotnet/sdk:8.0 \
                  ls -R
                '''

                sh '''
                docker run --rm \
                  -v $PWD:/app \
                  -w /app \
                  mcr.microsoft.com/dotnet/sdk:8.0 \
                  dotnet build ~/DotNet-8-Crud-Web-API-Example/DotNetCrudWebApi
                '''
            }
        }

    }
}
