pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Clona o repositório Git
                git 'https://github.com/Ansoferreiro/Testes'
            }
        }
        stage('Run Tests') {
            steps {
                // Instala dependências (opcional, depende de seu setup)
                sh 'pip install -r requirements.txt'
                
                // Executa os testes automatizados
                sh 'python3 test_android_device.py'
            }
        }
    }
    post {
        always {
            // Arquiva os resultados de teste no Jenkins
            junit '**/test-reports/*.xml'
        }
    }
}

