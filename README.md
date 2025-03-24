# 📡 Minitalk - Interprocess Communication in Unix

![Minitalk](https://img.shields.io/badge/Language-C-blue) ![Makefile](https://img.shields.io/badge/Tool-Makefile-yellow) ![Norminette](https://img.shields.io/badge/Style-Norminette-green)

The **Minitalk** project aims to explore the fundamentals of interprocess communication in Unix systems, using signals as a means of exchanging information. Through this project, students develop a simple communication program that uses **SIGUSR1** and **SIGUSR2** signals to send messages between two processes.

---

## 📋 Project Objective

🔹 Develop two programs:  
1. **Server**: waits for incoming signals and interprets the received data.  
2. **Client**: sends messages to the server using Unix signals.  

🔹 **Understand interprocess communication** in Unix systems.  
🔹 Work with **signals** and learn how to use them to transmit data.  
🔹 Explore **Unix system functions**, such as `kill()` and `signal()`.  
🔹 Implement **input/output redirection** and efficiently manage processes.

---

## 📚 Main Concepts

- 🔄 **Interprocess Communication**: exchanging messages between client and server via signals.  
- 📡 **Unix Signals**: using **SIGUSR1** and **SIGUSR2** to encode and transmit messages.  
- 🧵 **Signal Management**: handling signals using Unix system functions (`kill()`, `signal()`, etc.).  
- 📂 **Input/Output Redirection**: managing streams to control data input and output.  
- ⏱️ **Synchronization**: ensuring proper reception and decoding of sent messages.

---

## ✨ Implemented Features

### 🔧 Program Structure
1. **Server**  
   - Starts by waiting for client connections.  
   - Receives **SIGUSR1** and **SIGUSR2** signals, decodes the data, and displays the received message.  
   - Displays its **PID** (Process ID) so the client knows where to send the signals.  

2. **Client**  
   - Sends a text message to the server by converting each character into a sequence of signals.

### 🛠️ Technical Features
- **Message Encoding**:  
   - Each character of the message is converted to binary and sent to the server bit by bit using signals.

- **Server Decoding**:  
   - Received signals are interpreted and reconstructed to display the original message.

- **Error Handling**:  
   - Validates the PID and the message format.  
   - Handles lost signals or interruptions.

---

## 🛠️ Tools and Standards

| Tool/Standard         | Description                                                        |
|-----------------------|--------------------------------------------------------------------|
| **GIT**               | Version control to organize the development of the code.           |
| **Makefile**          | Automates compilation and generation of executables.               |
| **Norminette**        | Ensures compliance with the 42 coding style standards.             |

---


