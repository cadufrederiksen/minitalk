# 📡 Minitalk - Comunicação entre Processos em Unix

![Minitalk](https://img.shields.io/badge/Language-C-blue) ![Makefile](https://img.shields.io/badge/Tool-Makefile-yellow) ![Norminette](https://img.shields.io/badge/Style-Norminette-green)

O projeto **Minitalk** tem como objetivo explorar os fundamentos da comunicação entre processos no sistema Unix, utilizando sinais como meio de troca de informações. Por meio deste projeto, os estudantes desenvolvem um programa de comunicação simples que utiliza sinais **SIGUSR1** e **SIGUSR2** para enviar mensagens entre dois processos.

---

## 📋 Objetivo do Projeto

🔹 Desenvolver dois programas:  
1. **Servidor**: aguarda sinais de entrada e interpreta os dados recebidos.  
2. **Cliente**: envia mensagens para o servidor por meio de sinais de Unix.  

🔹 **Compreender a comunicação entre processos** em sistemas Unix.  
🔹 Trabalhar com **sinais** e entender como utilizá-los para transmitir dados.  
🔹 Explorar **funções do sistema Unix**, como `kill()` e `signal()`.  
🔹 Implementar **redireção de entrada/saída** e gerenciar processos de forma eficiente.

---

## 📚 Conceitos Principais

- 🔄 **Comunicação entre Processos**: troca de mensagens entre cliente e servidor por sinais.  
- 📡 **Sinais de Unix**: uso de **SIGUSR1** e **SIGUSR2** para codificar e transmitir mensagens.  
- 🧵 **Gestão de Sinais**: manipulação de sinais com funções do sistema Unix (`kill()`, `signal` etc.).  
- 📂 **Redireção de Entrada/Saída**: manipulação de streams para controlar dados de entrada e saída.  
- ⏱️ **Sincronização**: garantir a correta recepção e decodificação das mensagens enviadas.  

---

## ✨ Funcionalidades Implementadas

### 🔧 Estrutura do Programa
1. **Servidor**  
   - Inicia aguardando conexões de clientes.  
   - Recebe sinais **SIGUSR1** e **SIGUSR2**, decodifica os dados e exibe a mensagem recebida.  
   - Exibe o **PID** (Process ID) para que o cliente saiba onde enviar os sinais.  

2. **Cliente**  
   - Envia uma mensagem de texto para o servidor, convertendo cada caractere em uma sequência de sinais.  

### 🛠️ Funcionalidades Técnicas
- **Codificação de Mensagens**:  
   - Cada caractere da mensagem é convertido para binário e enviado ao servidor bit a bit utilizando sinais.  

- **Decodificação no Servidor**:  
   - Os sinais recebidos são interpretados e reconstruídos para exibir a mensagem original.  

- **Gestão de Erros**:  
   - Validação do PID e do formato da mensagem.  
   - Tratamento de sinais perdidos ou interrupções.  

---

## 🛠️ Ferramentas e Padrões

| Ferramenta/Padrão      | Descrição                                               |
|-------------------------|-------------------------------------------------------|
| **GIT**                | Controle de versão para organizar o desenvolvimento do código. |
| **Makefile**           | Automação da compilação e geração dos executáveis.      |
| **Norminette**         | Garantia de conformidade com os padrões de estilo da 42. |

---

