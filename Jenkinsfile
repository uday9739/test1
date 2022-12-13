pipeline {

    agent any

    stages {


    stage('Build Deploy Code') {
            when {
                branch 'development'
            }
            steps {
                scp . root@34.100.165.150:/var/www/html/
                ssh sh pm2 start index.js
                echo "Building Artifact"
                """

                sh """
                echo "Deploying Code"
                """
            }
        }

    }
  }
