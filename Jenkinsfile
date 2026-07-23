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
                bat 'javac hello.java'
            }
        }
        stage ('Run'){
            steps{
                echo 'Running Java Program....'
                bat 'java hello'
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