pipeline {
    agent any

    stages {
        stage('Build') {
          agent {
            docker {
              image 'node:20.9.0'
              reuseNode true
            }
          }
            steps {
                sh '''
                  ls -la
                  node --version
                  npm --version
                  npm install -g @angular/cli
                  npm install
                  npm run build
                  cp -r dist/jenkins-angular-app-test /var/www/
                  ls -la
                  pwd
                '''
            }
        }
    }
}
