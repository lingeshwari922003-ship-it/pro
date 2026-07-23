pipeline{
    agent any
    stages{
        stage('checkout'){
            steps{
                echo 'Getting source code...'
                checkout scm
            }
        }
        stage ('compile'){
            steps{
                echo 'compiling Java Program....'
                bat 'javac Hello.java'
            }
        }
        stage ('Run'){
            steps{
                echo 'Running Java Program....'
                bat 'java Hello'
            }
        }
    }
    post{
        always{
            echo 'pipeline completed'
        }
        success{
            echo 'Build successfully'
        }
        failure{
            echo 'Build failed'
        }
    }
}