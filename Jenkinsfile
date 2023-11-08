pipeline {
    agent any

    stages {
        
        stage('kurva') {
            when {
                expression {
                    kurva == 'true'
                }
            }
            steps {
                script {
                    sh 'echo "kurva!"'
                }
            }
        }
        stage('production') {
            when {
                expression {
                    branch == 'refs/heads/production'
                }
            }
            steps {
                script {
                    sh 'echo "production line kurva!"'
                }
            }
        }
        stage('staging') {
            when {
                expression {
                    branch == 'refs/heads/staging'
                }
            }
            steps {
                script {
                    sh 'echo "staging kurva!"'
                }
            }
        }
    }
}
