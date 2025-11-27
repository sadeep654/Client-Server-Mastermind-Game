<!-- Repository Banner -->
<p align="center">
  <img src="img/banner.png" width="100%" alt="Project Banner" />
</p>

---

## 🔹 Overview
This project implements a multi-player Mastermind game using **a client–server architecture in C**, demonstrating practical skills in **network programming, concurrency handling, and real-time communication**. It was built on Linux using **TCP for control messages and UDP for gameplay**, showcasing strong understanding of low-level socket operations and system programming.

<!-- Badges -->
<p>
  <img src="https://img.shields.io/badge/Language-C-blue.svg" />
  <img src="https://img.shields.io/badge/Platform-Linux-green.svg" />
  <img src="https://img.shields.io/badge/Network-TCP%2FUDP-orange.svg" />
  <img src="https://img.shields.io/badge/Build-Makefile-yellow.svg" />
  <img src="https://img.shields.io/badge/Status-Stable-brightgreen.svg" />
</p>

---

## 🔹 Architecture

<p align="center">
  <img src="img/diagram.png" width="80%" alt="Client-Server Architecture Diagram" />
</p>

**Architecture Summary**
- **TCP:** Login, commands, matchmaking, state updates  
- **UDP:** Real-time gameplay messaging  
- **Server:** Tracks online players, pending requests, game sessions  
- **Clients:** Handle gameplay logic + UI interaction  

---

## 🔹 Gameplay Demo

<p align="center">
  <img src="demo.gif" width="70%" alt="Gameplay Demo GIF" />
</p>

*(To create your own GIF: record gameplay using OBS or Peek → save as demo.gif → upload to repo.)*

---

## 🔹 Key Features
- 🌐 **Client–server architecture** using TCP & UDP  
- 🧩 Turn-based Mastermind gameplay  
- 🕒 **60-second timeout system**  
- 👥 Multi-client support  
- 📝 Command-based interface  
- 🛡️ Username & session validation  
- 🔄 Real-time updates between two players  

>### ✔ Supported Commands
| Command | Description |
|--------|-------------|
| `!help` | Show all commands |
| `!who` | List online players |
| `!start <user>` | Send a match request |
| `!accept` / `!reject` | Respond to match requests |
| `!combination` | Submit your guess |
| `!disconnect` | Leave the match |
| `!quit` | Exit the server |

---

## 🔹 Installation & Build

>### 🔧 Requirements
- Linux OS (Ubuntu, Fedora, etc.)  
- GCC Compiler  
- Make utility  

>### 🛠 Build the Project
```bash
# Compile
make -f makefile

# Run server
./MServer 127.0.0.1 1234

# Run client (in new terminal)
./MClient 127.0.0.1 1234
