pipeline{
    agent any
    stages {
        stage('setup'){
            steps{
                echo 'installing dependencies'
                bat 'python -m pip install requirements.txt'
            }
        }
        stage('build and test'){
            steps{
                echo 'runnig ml pipeline'
                bat 'python ml_pipeline.py'
            }
        }
    }
    post{
        success{
            echo 'model success'
        }
        failure{
            echo 'model failed'
        }
    }
}