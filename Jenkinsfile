pipeline {
    agent any

    tools {
        nodejs 'njs-211'
    }

    environment {
        CI = false
        OCI_CLI_SUPPRESS_FILE_PERMISSIONS_WARNING = true
    }

    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Deploy') {
            steps {
                sh '/var/lib/jenkins/bin/oci os object bulk-upload -ns axgl5hrae4r8 -bn cdjmdev_public --src-dir ./dist/ --overwrite --include *.html --content-type text/html'
                sh '/var/lib/jenkins/bin/oci os object bulk-upload -ns axgl5hrae4r8 -bn cdjmdev_public --src-dir ./dist/ --overwrite --include *.css --content-type text/css'
                sh '/var/lib/jenkins/bin/oci os object bulk-upload -ns axgl5hrae4r8 -bn cdjmdev_public --src-dir ./dist/ --overwrite --include *.png --content-type image/png'
                sh '/var/lib/jenkins/bin/oci os object bulk-upload -ns axgl5hrae4r8 -bn cdjmdev_public --src-dir ./dist/ --overwrite --include *.jpg --content-type image/jpg'
                sh '/var/lib/jenkins/bin/oci os object bulk-upload -ns axgl5hrae4r8 -bn cdjmdev_public --src-dir ./dist/ --overwrite --include *.ico --content-type image/vnd.microsoft.icon'
                sh '/var/lib/jenkins/bin/oci os object bulk-upload -ns axgl5hrae4r8 -bn cdjmdev_public --src-dir ./dist/ --overwrite --include "js/*.js" --content-type text/javascript'
                sh '/var/lib/jenkins/bin/oci os object bulk-upload -ns axgl5hrae4r8 -bn cdjmdev_public --src-dir ./dist/ --overwrite --include "*.svg" --content-type image/svg+xml'
            }
        }
    }

    post {
        always {
            cleanWs()
        }
    }
}