# ⚡ Automating Collaborative Development Workflow with Bash 🚀  
**Development Operations - Assignment 01**  
📌 *By: 2022132 - Ayesha Kashif & 2022485 - Noor ul Ain*  

<div align="center">
  <img src="https://media.giphy.com/media/26tn33aiTi1jkl6H6/giphy.gif" width="200"/>
</div>  

---

## 🛠️ **Project Overview**  
Welcome to our *fully automated* development workflow! This Bash script is designed to streamline **collaborative coding** by:  
✅ Monitoring file changes 🔍  
✅ Automating Git commits & pushes 🔄  
✅ Sending real-time email notifications 📩  

*Because let’s be honest, who wants to manually commit and push code every 10 minutes?* 😅  

---

## 🌟 **Features**  
🎯 **Smart Change Detection** – Uses SHA-256 checksums to track changes.  
🎯 **Git Automation** – Auto-stages, commits, and pushes to your repo.  
🎯 **Instant Notifications** – Sends alerts to collaborators via SendGrid API.  
🎯 **Easy Customization** – Configurable `config.cfg` file for project settings.  
🎯 **Built-in Error Handling** – Manages Git failures, API issues & monitoring errors.  

---

## 📂 **Project Structure**  
```sh
📂 /automation_script   # Contains the Bash script
📂 /config              # Configuration settings (config.cfg)
📂 /docs                # Documentation and README
```

---

## 🏗️ **Setup & Installation**  
### 🔹 **1. Clone the Repository**  
```sh
git clone https://github.com/ayeshakashif-ak/auto-devops.git
cd auto-devops
```

### 🔹 **2. Configure Your Settings**  
Edit the `config.cfg` file to match your repo settings:  
```sh
# Path to the local Git repository
REPO_PATH="/absolute/path/to/repo"

# File or directory to monitor
MONITOR_PATH="/absolute/path/to/monitor"

# Git settings
GIT_REMOTE="origin"
BRANCH="main"

# SendGrid API settings
SENDGRID_API_KEY="your_api_key_here"
SENDER_EMAIL="you@example.com"

# Collaborators' email addresses
COLLABORATORS="collab1@example.com, collab2@example.com"
```

### 🔹 **3. Run the Script**  
Make it executable & start monitoring:  
```sh
chmod +x monitor_and_push.sh
./monitor_and_push.sh
```

---

## 🎯 **How It Works**  
1️⃣ Watches the specified file/directory for changes.  
2️⃣ Generates an SHA-256 checksum to detect modifications.  
3️⃣ Stages, commits, and pushes updates to GitHub.  
4️⃣ Sends an email notification to all team members.  
5️⃣ Runs forever… until you decide it’s time to stop! 😆  

---

## 🛑 **Error Handling**  
✅ **Git Push Failures?** The script retries! 🔄  
✅ **SendGrid API Issues?** Logs errors & alerts user! 🚨  
✅ **File Monitoring Problems?** Warns if the directory is inaccessible! ⚠️  

---

## 👥 **Meet the Team**  
🎓 **Ayesha Kashif** - Automation Enthusiast 🤖  
🎓 **Noor ul Ain** - Git & CI/CD Ninja 🏆  

---

## 📜 **License**  
This project is built for educational purposes. Feel free to **fork, learn, and modify** – but no commercial use! 🚀  

---

💡 *Collaboration just got easier! Let's code, commit, and conquer!* 🎯  
