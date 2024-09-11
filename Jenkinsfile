pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Clone the Git repository
                git url: 'https://github.com/satvik-balusu/static-website.git'
            }
        }
        stage('Deploy') {
            steps {
                // Copy static files to the web directory
                sh '''
                cp -r * /var/www/html/
                chown -R www-data:www-data /var/www/html/
                '''
            }
        }
    }
}
