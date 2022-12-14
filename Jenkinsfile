pipeline {

    agent any

    stages {


    stage('Build Deploy Code to development branch') {
            when {
                branch 'development'
            }
            steps {
                sh "scp index.js udaykumarbk@34.100.165.150:/home/udaykumarbk/"
                sh "ssh udaykumarbk@34.100.165.150 'sudo pm2 start index.js'"
            }
        }
        stage('Build Deploy the Codeto staging branch') {
            when {
                branch 'staging'
            }
            steps {
                sh "scp main.js udaykumarbk@34.100.165.150:/home/udaykumarbk/"
                sh "ssh udaykumarbk@34.100.165.150 'sudo pm2 start main.js'"
            }

    }
  }
}


