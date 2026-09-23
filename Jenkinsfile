pipeline{
    agent any
    stages{
        stage('checkout code'){
            steps{
                git branch:'main',url='https://github.com/rishabesh14/ass1.git'
            }
        }
        stage('Install dependencies'){
            steps{
                bat 'pip install -r requirements.txt' 
            }
        }
        stage('Run unit tests'){
            steps{
                bat 'pytest test_app.py'
            }
        }
    }
    post{
        success{
            echo 'Test successful'
        }
        failure{
            echo 'Test not successful'
        }
    }
}