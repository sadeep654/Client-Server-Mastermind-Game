<!-- Repository Banner -->
<p align="center">
  <img src="img/banner.png" width="100%" alt="Project Banner" />
</p>

---

## 🔹 Overview
This project implements a multi-player Mastermind game using **a client–server architecture in C**, demonstrating practical skills in **network programming, concurrency handling, and real-time communication**. It was built on Linux using **TCP for control messages and UDP for gameplay**, showcasing strong understanding of low-level socket operations and system programming.

<!-- Badges -->
<p align="center">
  <img alt="C" src="https://img.shields.io/badge/-C-A8B9CC?style=flat-square&logo=c&logoColor=black" />
  <img alt="Linux" src="https://img.shields.io/badge/-Linux-FCC624?style=flat-square&logo=linux&logoColor=black" />
  <img alt="Ubuntu" src="https://img.shields.io/badge/-Ubuntu-E95420?style=flat-square&logo=ubuntu&logoColor=white" />
  <img alt="TCP/UDP" src="https://img.shields.io/badge/-TCP%2FUDP-0078D6?style=flat-square&logo=network&logoColor=white" />
  <img alt="Makefile" src="https://img.shields.io/badge/-Makefile-000000?style=flat-square&logo=gnu&logoColor=white" />
  <img alt="Client-Server" src="https://img.shields.io/badge/-Client%20%2F%20Server-5A5A5A?style=flat-square&logo=serverless&logoColor=white" />
  <img alt="Apache" src="https://img.shields.io/badge/-Apache%202.0-D22128?style=flat-square&logo=apache&logoColor=white" />
  <img alt="Status" src="https://img.shields.io/badge/-Stable-4CAF50?style=flat-square&logo=vercel&logoColor=white" />
</p>
</p>

---

## 🔹 Architecture

<p align="center">
  <img src="img/diagram.png" width="100%" alt="Client-Server Architecture Diagram" />
</p>

>**Architecture Summary**
- **TCP:** Login, commands, matchmaking, state updates  
- **UDP:** Real-time gameplay messaging  
- **Server:** Tracks online players, pending requests, game sessions  
- **Clients:** Handle gameplay logic + UI interaction  

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
```

---

## 🔹 Project Structure
```bash
MServer.c      # Server program
MClient.c      # Client program
makefile       # Build instructions
README.md      # Documentation
```

---

## 🔹 Notes
- Developed and tested on Fedora Linux.
- Uses numerical symbols (0–9) instead of colours for Mastermind logic.
- Based on coursework requirements documented in the assignment.

---

## 📩 Contact

Feel free to explore, fork, or reach out for collaboration or opportunities.
