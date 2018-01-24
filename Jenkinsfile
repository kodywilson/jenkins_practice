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
        always {
            mail to: 'Kody.Wilson@nordstrom.com'
                subject: "Attempted Pipeline: ${currentBuild.fullDisplayName}",
                body: "Something happened to ${env.BUILD_URL}"
        }
    }
}

