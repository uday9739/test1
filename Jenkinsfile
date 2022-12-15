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
        stage('Build Deploy the Code to staging branch') {
            when {
                branch 'staging'
            }
            steps {
                sh "scp main.js udaykumarbk@34.100.165.150:/home/udaykumarbk/"
                sh "ssh udaykumarbk@34.100.165.150 'sudo pm2 start main.js'"
            }

    }
  }

post {
    success {
        slackSend channel: '#test_channel',
                  color: 'good',
                  message: "The pipeline ${currentBuild.fullDisplayName} completed successfully."
    }
    failure {
        slackSend channel: '#test_channel',
                  color: 'danger',
                  message: "The pipeline ${currentBuild.fullDisplayName} is got failed."
    }

}
}
