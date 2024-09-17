 {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Clona o repositório Git
                git 'https://github.com/Ansoferreiro/Testes.git'
            }
        }
        stage('Run Tests') {
            steps {
                // Instalar dependências (se necessário)
                sh 'pip install -r requirements.txt'
                
                // Executar o script de testes
                sh 'python3 test_android_device.py'
            }
        }
    }
    post {
        always {
            // Arquivar resultados dos testes
            junit '**/test-reports/*.xml'
        }
    }
}
