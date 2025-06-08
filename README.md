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

## Step 2: Add Jenkins Repository and Key
