pipeline {
    agent { docker 'ruby' }
    stages {
        stage('build') {
            steps {
                sh 'ruby --version'
                sh 'pwd'
                sh 'ls -la'
            }
        }
        stage('test') {
            steps {
                sh 'echo "Testing, testing, 1, 2, 3!"'
            }
        }
    }
    post {
        success {
            mail to: 'Kody.Wilson@nordstrom.com',
                subject: "Build Success: ${currentBuild.fullDisplayName}",
                body: "Pipeline Branch Build # ${currentBuild.fullDisplayName} - url - ${env.BUILD_URL}"
        }
    }
}

