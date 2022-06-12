pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        git(url: 'https://github.com/dinushchathurya/jenkins-nodejs-sample-project.git', branch: 'master')
      }
    }

    stage('bash') {
      steps {
        sh '''#!/bin/sh     
          ssh ubuntu@13.213.31.98 <  cd /var/www/jenkins-nodejs-sample-project 
          git pull origin master    
          npm install     
          pm2 restart all
          exit      
          EOF'''
      }
    }

  }
}