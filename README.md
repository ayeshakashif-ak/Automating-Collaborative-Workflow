# **Automating Collaborative Development Workflow Using Bash Scripting**  

<div id="header" align="center">
  <img src="https://media.giphy.com/media/M9gbBd9nbDrOTu1Mqx/giphy.gif" width="100"/>
</div>  


## **Overview**  
This Bash script automates the process of monitoring a file or directory for changes, committing and pushing updates to a Git repository, and notifying collaborators via email using the **SendGrid API**. It ensures a seamless workflow in collaborative development environments by reducing manual intervention.  

---

## **Features**  
✅ **Automatic Change Detection** – Uses SHA-256 checksums to track file modifications.  
✅ **Git Automation** – Automatically stages, commits, and pushes changes to the remote repository.  
✅ **Email Notifications** – Sends real-time updates to collaborators via SendGrid.  
✅ **Configurable Settings** – Uses a `config.cfg` file for easy customization.  
✅ **Error Handling** – Manages Git failures, API issues, and monitoring errors.  

---

## **Prerequisites**  
Ensure you have the following installed before running the script:  

### **For Linux/macOS (WSL for Windows Users):**  
- **Git** ([Download & Install](https://git-scm.com/downloads))  
- **jq** (For JSON parsing: `sudo apt install jq` or `brew install jq`)  
- **inotify-tools** (For file monitoring: `sudo apt install inotify-tools` or `brew install fswatch`)  
- **SendGrid API Key** ([Get API Key](https://sendgrid.com))  

### **For Windows (Git Bash Users):**  
- **Git** ([Download](https://git-scm.com/downloads))  
- **jq** (Install via [Chocolatey](https://chocolatey.org/): `choco install jq`)  
- **SendGrid API Key** ([Get API Key](https://sendgrid.com))  
- **File Monitoring Alternative:** Use **PowerShell scripts** instead of `inotify-tools`.  

---

## **Installation & Setup**  

### **1. Clone the Repository**  
```sh
git clone <your-repository-url>
cd <your-repository-folder>
```

### **2. Configure the Script**  
Edit the `config.cfg` file to specify project settings:  

```sh
# Path to the local Git repository
REPO_PATH="/absolute/path/to/repository"

# File or directory to monitor
MONITOR_PATH="/absolute/path/to/monitor"

# Git settings
GIT_REMOTE="origin"
BRANCH="main"

# SendGrid Email API settings
SENDGRID_API_KEY="your_sendgrid_api_key"
SENDER_EMAIL="your_email@example.com"

# Collaborators to notify (comma-separated emails)
COLLABORATORS="collaborator1@example.com,collaborator2@example.com"
```

### **3. Run the Script**  
Make the script executable and start monitoring changes:  

```sh
chmod +x monitor_and_push.sh
./monitor_and_push.sh
```

---

## **How It Works**  

1️⃣ **Monitors** the specified file/directory for changes.  
2️⃣ **Calculates a checksum** (SHA-256) to detect modifications.  
3️⃣ **Commits and pushes changes** automatically to the GitHub repository.  
4️⃣ **Sends email notifications** to collaborators about updates.  

---

## **Error Handling**  
The script includes error handling for:  
🚨 **Git Push Failures** – Detects and retries failed pushes.  
🚨 **SendGrid API Errors** – Logs failed email notifications.  
🚨 **File Monitoring Issues** – Alerts if the specified directory is inaccessible.  

---

## **Testing & Logs**  
To verify functionality, you can check:  

- **Git Log:**  
  ```sh
  git log --oneline -n 5
  ```
- **Script Logs:**  
  Check `monitor.log` (if implemented) for monitoring and error messages.  

---

## **Contributing**  
Feel free to submit **pull requests** or **issues** to improve the script! 🚀  

---

## **License**  
This project is open-source under the **MIT License**.  

---

### **Need Help?**  
📧 Contact: your_email@example.com  
