pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
              sh 'docker build -t tapanmicroservice .'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
              sh 'docker rm -f tapanmicroservice || true'
              sh 'docker run -d -p 3000:3000 --name tapanmicroservice tapanmicroservice'
            }
        }
    }
}
