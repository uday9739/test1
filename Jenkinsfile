pipeline {

    agent any

    stages {


    stage('Build Deploy Code') {
            when {
                branch 'development'
            }
            steps {
                sh "scp . root@34.100.165.150:/var/www/html/"
                sh "pm2 start index.js"
                echo "Building Artifact"
                """

                sh """
                echo "Deploying Code"
                """
            }
        }

    }
  }
