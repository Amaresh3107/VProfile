# VProfile – DevOps Infrastructure Automation Project

This repository focuses on DevOps infrastructure setup, provisioning, and automation
for a multi-tier application using Vagrant and Ansible.

🚫 Application source code is not developed by me.  
✅ My work focuses on infrastructure automation, service configuration, and environment reproducibility.

---

## 🎯 Project Objective

- Build a real-world multi-tier application environment locally
- Automate VM creation using Vagrant
- Provision and configure services using shell scripts and Ansible
- Understand service dependencies and infrastructure design

---

## 🧱 Architecture Overview

**Components used:**

- Web Server: Nginx
- Application Server: Tomcat
- Database: MySQL
- Cache: Memcached
- Message Queue: RabbitMQ

Each component runs on a separate virtual machine.

---

## ⚙️ Tools & Technologies

- Vagrant
- VirtualBox
- Ansible
- Linux
- Nginx
- Tomcat
- MySQL
- RabbitMQ
- Memcached
- Git

---

## Database
Here,we used Mysql DB 
sql dump file:
- /src/main/resources/db_backup.sql
- db_backup.sql file is a mysql dump file.we have to import this dump to mysql db server
- > mysql -u <user_name> -p accounts < db_backup.sql

---

## 🔁 Provisioning Flow

Service startup order:

1. MySQL  
2. Memcached  
3. RabbitMQ  
4. Tomcat  
5. Nginx  

This ensures proper dependency handling.

---

## 🤖 Automation Details

- Multi-VM creation using Vagrant
- Manual and automated provisioning approaches
- Configuration management using Ansible
- Repeatable and consistent local environment

---

## 🚀 How to Run

### Automated Provisioning

This method sets up the complete infrastructure and services automatically.

```bash
git clone https://github.com/<your-username>/VProfile.git
cd VProfile/vagrant/Automated_provisioning_MacOSM1
vagrant up

Once provisioning is complete, access the application from your browser using the
Nginx VM IP address: 
http://192.168.56.21

---

## 🛠️ Manual Provisioning

This approach creates the infrastructure using Vagrant,
and services are installed and configured manually step by step.

```bash
git clone https://github.com/<your-username>/VProfile.git
cd VProfile/vagrant/Manual_provisioning_MacOSM1
vagrant up

After the VMs are up, follow the complete step-by-step setup guide provided in the documentation:

Once manual setup is completed, access the application using the Nginx VM IP address:
http://192.168.56.21
