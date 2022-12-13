pipeline {

    agent any

    stages {


    stage('Build Deploy the Code') {
            when {
                branch 'development'
            }
            steps {
                sh "scp -r . root@34.100.165.150:/var/www/html/"
                sh "pm2 start index.js"
            }
        }

    }
  }
