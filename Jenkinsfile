pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
   stage('Init') {
	steps {
	 git branch: 'master',
	 url: 'https://github.com/pocteo/nodejs_app.git'
      }
    }

    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }

    stage('publish package to npmjs') {
      steps {
        sh 'npm publish --access=public'
       }
    }
  }
}
