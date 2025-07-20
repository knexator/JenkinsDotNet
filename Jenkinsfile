pipeline {
    agent any

    stages {
        stage ('Checkout') {
            steps {
                cleanWs()
                bat "git clone https://github.com/knexator/JenkinsDotNet.git ."
            }
        }
        stage ('Tests') {
            steps {
                bat "dotnet test --configuration Release --no-build --logger trx --results-directory TestResults"
            }
        }
    }
}