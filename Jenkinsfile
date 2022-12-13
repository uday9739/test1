pipeline {

    agent any
    
    stages {
    
    
    stage('Build Deploy Code') {
            when {
                branch 'development'
            }
            steps {
                sh pm2 start index.js
                echo "Building Artifact"
                """

                sh """
                echo "Deploying Code"
                """
            }
        }

    } 
  }  
