# Jenkins Installation Guide on Ubuntu 20.04 with Java 17

This guide explains how to install Jenkins on Ubuntu 20.04 using OpenJDK 17.

---

## Prerequisites

- Ubuntu 20.04 LTS
- Internet access
- Sudo privileges
- Port 8080 open

---

## Step 1: Install Java 17

```bash
sudo apt update
sudo apt install -y openjdk-17-jdk
java -version
```
## Step 2: Add Jenkins Repository and Key
```bash
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt update
```
## Step 3: Install Jenkins
```bash
sudo apt install -y jenkins
```
## Step 4: Start and Enable Jenkins Service
```bash
sudo systemctl start jenkins
sudo systemctl enable jenkins
sudo systemctl status jenkins
```
## Step 5: Access Jenkins UI
Open your web browser and go to: http://localhost:8080
(Replace localhost with your server IP if remote.)
## Step 6: Retrieve Initial Admin Password
```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
Copy and paste this password into the Jenkins web UI to unlock Jenkins.
```
## Step 7: Complete Jenkins Setup Wizard
Install suggested plugins

Create the first admin user

Configure instance URL (optional)
##  Step 8 (Optional): Open Firewall Port 8080
sudo ufw allow 8080
sudo ufw reload

## Useful Commands
```bash
sudo systemctl start jenkins	  Start Jenkins
sudo systemctl stop jenkins	    Stop Jenkins
sudo systemctl restart jenkins	Restart Jenkins
sudo systemctl status jenkins	  Check Jenkins status
sudo journalctl -u jenkins -f	  Follow Jenkins logs
```
## Important Jenkins Paths
- Jenkins home directory: `/var/lib/jenkins`
- Jenkins config file: `/etc/default/jenkins`
- Jenkins log file: `/var/log/jenkins/jenkins.log`

