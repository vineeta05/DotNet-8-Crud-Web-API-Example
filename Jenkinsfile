stage('Build .NET Project') {
    steps {

        sh """
        docker run --rm \
          -v ${WORKSPACE}:/app \
          -w /app \
          mcr.microsoft.com/dotnet/sdk:8.0 \
          ls -R
        """

        sh """
        docker run --rm \
          -v ${WORKSPACE}:/app \
          -w /app \
          mcr.microsoft.com/dotnet/sdk:8.0 \
          dotnet build
        """
    }
}
