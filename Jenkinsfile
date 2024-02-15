pipeline {
    agent any

    tools {
        nodejs 'njs-211'
    }

    environment {
        CI = false
        OCI_CLI_SUPPRESS_FILE_PERMISSIONS_WARNING = true
        GENERATE_SOURCEMAP = false
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
                sh '/var/lib/jenkins/bin/oci os object bulk-upload -ns axgl5hrae4r8 -bn cdjmdev_public --src-dir ./dist/ --overwrite --include *.txt --content-type text/plain'
                sh '/var/lib/jenkins/bin/oci os object bulk-upload -ns axgl5hrae4r8 -bn cdjmdev_public --src-dir ./dist/ --overwrite --include *.css --content-type text/css'
                sh '/var/lib/jenkins/bin/oci os object bulk-upload -ns axgl5hrae4r8 -bn cdjmdev_public --src-dir ./dist/ --overwrite --exclude vue.config.js babel.config.js --include *.js --content-type text/javascript'
                sh '/var/lib/jenkins/bin/oci os object bulk-upload -ns axgl5hrae4r8 -bn cdjmdev_public --src-dir ./dist/ --overwrite --include *.png --content-type image/png'
                sh '/var/lib/jenkins/bin/oci os object bulk-upload -ns axgl5hrae4r8 -bn cdjmdev_public --src-dir ./dist/ --overwrite --include *.ico --content-type image/vnd.microsoft.icon'
            }
        }
    }

    post {
        always {
            cleanWs()
        }
    }
}