Projeto de Automação de Testes Android com Jenkins
Descrição
Este projeto configura uma pipeline de automação para testar um dispositivo Android usando Jenkins e Git. O objetivo é executar testes automatizados em um dispositivo Android, garantindo a integração contínua e a entrega contínua de aplicativos Android.

Ferramentas e Tecnologias Utilizadas
Jenkins: Ferramenta de integração contínua e entrega contínua (CI/CD) que automatiza a execução de testes e builds.
Git: Sistema de controle de versão distribuído para gerenciar o código fonte e o histórico do projeto.
Android SDK: Conjunto de ferramentas necessárias para o desenvolvimento e teste de aplicativos Android.
ADB (Android Debug Bridge): Ferramenta de linha de comando que permite a comunicação com dispositivos Android.
SDK Command Line Tools: Ferramentas de linha de comando para gerenciar o SDK e os componentes do Android.
Python: Linguagem de programação usada para escrever scripts de teste.
unittest: Framework de teste de unidade para Python, utilizado para organizar e executar os testes.
Appium (Opcional): Ferramenta de automação para testes de interface gráfica em dispositivos Android e iOS.
Appium Python Client: Biblioteca para escrever testes com Appium usando Python.
Estrutura do Projeto
test_android_device.py: Script de teste em Python que usa ADB para verificar o estado do dispositivo Android. Inclui:
Verificação se um dispositivo Android está conectado.
Teste para verificar se a tela do dispositivo está ligada.
Jenkinsfile: Arquivo de configuração do Jenkins Pipeline. Define as etapas do pipeline, que incluem:
Checkout: Clona o repositório Git.
Run Tests: Instala dependências e executa os testes automatizados.
Post Build Actions: Arquiva os resultados dos testes.
Passos para Configuração
Configuração do Jenkins:

Instalar os plugins necessários: Git Plugin e Pipeline Plugin.
Configurar um novo Pipeline Job no Jenkins e apontar para o repositório Git.
Instalação do Android SDK:

Baixar as ferramentas de linha de comando do Android SDK.
Instalar e configurar o SDK Command Line Tools.
Usar o sdkmanager para instalar componentes necessários, como plataformas e build-tools.
Configuração do Ambiente de Teste:

Conectar um dispositivo Android via USB ou usar um emulador.
Instalar Python e o framework de teste unittest.
Configurar Appium, se necessário, para testes de interface gráfica.
Configuração do Repositório Git:

Criar um repositório no GitHub ou GitLab e fazer o push dos arquivos do projeto.
Execução e Monitoramento:

Executar o job no Jenkins para validar a configuração e garantir que os testes estejam funcionando conforme esperado.
Como Executar
No Jenkins:

Configure o Pipeline Job com o Jenkinsfile.
Execute o job e verifique os resultados dos testes na interface do Jenkins.
No Python:

Execute o script de teste diretamente para validar o funcionamento localmente.

Observações

Certifique-se de que o adb está corretamente configurado no PATH do sistema.
Assegure-se de que todos os componentes do Android SDK necessários estejam instalados.
Para testar a interface gráfica com Appium, ajuste o código conforme necessário para o seu aplicativo e ambiente de teste.
