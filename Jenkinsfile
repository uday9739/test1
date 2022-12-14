pipeline {

    agent any

    stages {


    stage('Build Deploy the Code') {
            when {
                branch 'development'
            }
            steps {
                sh "scp index.js udaykumarbk@34.100.165.150:/home/udaykumarbk/"
                sh "ssh udaykumarbk@34.100.165.150 'sudo pm2 start index.js'"
            }
        }

    }
  }
