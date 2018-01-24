pipeline {
    agent { docker 'ruby' }
    stages {
        stage('build') {
            steps {
                sh 'ruby --version'
                sh 'pwd'
                sh 'ls -la'
                sh 'echo "Testing, testing, 1, 2, 3!"'
            }
        }
    }
}

