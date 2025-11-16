pipeline{
    agent any

    stages{
        stage('Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/Ahmadfachri12/my-pipeline.git'
            }
        }

        stage('Build'){
            steps{
                sh 'docker build -t myapp .'
            }
        }

        stage('Test'){
            steps{
                sh 'echo "Running Testt...."'
            }
        }

        stage('Deploy'){
            steps{
                sh 'docker run -d -p 9000:80 --name myapp container-app'
            }
        }
    }
}
