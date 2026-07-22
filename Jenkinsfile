Pipeline{
    agent any
    stages{
        stage('checkout'){
            steps{
                echo 'Getting Source code.....'
                checkout scm
            }
        }
        stage('compile'){
            steps{
                echo 'compiling Java Program...'
                bat 'javac hello.java'
            }
        }
        stage('Run'){
            steps{
                echo 'Running Java Program...'
                bat 'java hello'
            }
        }
    }
    Post{
            always{
                echo 'Pipeline completed'
            }
            success{
                echo 'Build Successful'
            }
            failure{
                echo 'Build Failed'
            }
        }
    }