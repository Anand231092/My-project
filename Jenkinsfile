// Jenkinsfile (Declarative Pipeline)
pipeline {
  agent any

  pipeline {
  agent { label 'linux' }
  ...
}


  triggers {
    // optional: periodic fallback
    pollSCM('H/5 * * * *')
  }

  stages {
    stage('Checkout') {
      steps {
        // Uses the same SCM configuration as the job
        checkout scm
      }
    }

    stage('Build') {
      steps {
        sh 'echo "No build step for static site"'
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

  post {
    always {
      echo "Build finished."
    }
  }
}
