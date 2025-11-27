# Client-Server-Mastermind-Game

<!-- Repository Banner -->
<p align="center">
  <img src="banner.png" width="100%" alt="Project Banner" />
</p>

# 🎮 Mastermind Client–Server Game
A multiplayer Mastermind game implemented in **C** using **TCP** and **UDP** sockets.  
Features real-time communication, matchmaking, timeouts, and a command-based terminal interface.

<!-- Badges -->
<p>
  <img src="https://img.shields.io/badge/Language-C-blue.svg" />
  <img src="https://img.shields.io/badge/Platform-Linux-green.svg" />
  <img src="https://img.shields.io/badge/Network-TCP%2FUDP-orange.svg" />
  <img src="https://img.shields.io/badge/Build-Makefile-yellow.svg" />
  <img src="https://img.shields.io/badge/Status-Stable-brightgreen.svg" />
</p>

---

## 📘 Overview
This project implements a **client–server multiplayer Mastermind game** using low-level socket programming under Linux.  
The server manages all connected clients, matchmaking requests, username validation, and game session coordination.  
Clients communicate with the server via **TCP**, while gameplay exchanges occur using **UDP**.

---

## 🧱 Architecture

<p align="center">
  <img src="architecture.png" width="80%" alt="Client-Server Architecture Diagram" />
</p>

**Architecture Summary**
- **TCP:** Login, commands, matchmaking, state updates  
- **UDP:** Real-time gameplay messaging  
- **Server:** Tracks online players, pending requests, game sessions  
- **Clients:** Handle gameplay logic + UI interaction  

---

## 🎥 Gameplay Demo

<p align="center">
  <img src="demo.gif" width="70%" alt="Gameplay Demo GIF" />
</p>

*(To create your own GIF: record gameplay using OBS or Peek → save as demo.gif → upload to repo.)*

---

## 🚀 Features
- 🌐 **Client–server architecture** using TCP & UDP  
- 🧩 Turn-based Mastermind gameplay  
- 🕒 **60-second timeout system**  
- 👥 Multi-client support  
- 📝 Command-based interface  
- 🛡️ Username & session validation  
- 🔄 Real-time updates between two players  

### ✔ Supported Commands
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

## 📦 Installation & Build

### 🔧 Requirements
- Linux OS (Ubuntu, Fedora, etc.)  
- GCC Compiler  
- Make utility  

### 🛠 Build the Project
```bash
git clone https://github.com/<your-username>/Client-Server-Mastermind-Game.git
cd Client-Server-Mastermind-Game
make -f makefile
