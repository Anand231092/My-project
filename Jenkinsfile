pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                sudo rm -rf /usr/share/nginx/html/*
                sudo cp -r * /usr/share/nginx/html/
                '''
            }
        }
    }
<<<<<<< HEAD
}
=======
}
>>>>>>> f91de573645437df78221cf07d18ebc28dc1681e
