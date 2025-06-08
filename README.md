# Jenkins Installation Guide for Ubuntu 20.04

This guide explains how to install Jenkins on **Ubuntu 20.04 LTS** using the official Jenkins package repository. Follow the steps below to get Jenkins up and running quickly.

---

## 🛠️ Prerequisites

- Ubuntu 20.04 LTS
- A user account with `sudo` privileges
- Internet access
- Port `8080` open (or configure another port)

---

## 📦 Step 1: Install Java

Jenkins requires Java (preferably Java 11).

### Install OpenJDK 11:

```bash
sudo apt update
sudo apt install openjdk-11-jdk -y
