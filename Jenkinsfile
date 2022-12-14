pipeline {

    agent any

    stages {


    stage('Build Deploy the Code') {
            when {
                branch 'development'
            }
            steps {
                sh "scp -i ~/.ssh/id_rsa.pub Jenkinsfile udaykumarbk@34.100.165.150:/home/udaykumarbk/"
                sh "pm2 start index.js"
            }
        }

    }
  }
