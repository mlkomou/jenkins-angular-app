pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
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
