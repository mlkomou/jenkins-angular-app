pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
                  nvm use v20.9.0
                  node --version
                  npm --version
                  npm install -g @angular/cli
                  npm install
                  npm run build
                  cp -r dist/jenkins-angular-app-test /var/www/jenkins-test
                  ls -la
                  pwd
                '''
            }
        }
    }
}
