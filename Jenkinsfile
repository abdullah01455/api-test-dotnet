pipeline {
    agent any
   
    stages {
        stage('Restore') {
            steps {

                sh "dotnet restore"

            }
        }

        stage('Build') {
            steps {
                
                sh "dotnet build"

            }
        }

        stage('Test') {
            steps {
                
                sh 'dotnet sonarscanner end /d:sonar.login="sqp_214021e806165559144e4a20701b0237627c647a"'

            }

        }
       
    }
}