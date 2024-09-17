pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Ansoferreiro/Testes'
            }
        }
        stage('Run Tests') {
            steps {
                script {
                    // Comando para executar os testes
                    sh './run_tests.sh'
                }
            }
        }
        stage('Publish Test Results') {
            steps {
                junit '**/target/test-*.xml'
            }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: '**/target/*.apk', allowEmptyArchive: true
        }
    }
}

