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
                    branch == 'production'
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
                    branch == 'staging'
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
