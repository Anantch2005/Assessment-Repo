# AWS DevOps Engineer Internship Assignment

## Objective

The objective of this assignment is to deploy a simple static website on an AWS EC2 Ubuntu instance using Nginx and demonstrate basic Linux, AWS, Git, and Docker skills.

---

## Technologies Used

* AWS EC2 (Ubuntu)
* AWS Security Groups
* Linux (Ubuntu)
* Nginx
* Git & GitHub
* Docker (Bonus)

---

## Task 1 - Launch an EC2 Instance

An Ubuntu EC2 instance was launched on AWS. A Security Group was created with the following inbound rules:

| Port | Protocol | Purpose              |
| ---- | -------- | -------------------- |
| 22   | SSH      | Remote server access |
| 80   | HTTP     | Website access       |

The instance was accessed securely using SSH.

Example command:

```bash
ssh -i <key-file>.pem ubuntu@<EC2-Public-IP>
```

---

## Task 2 - Linux Basics

The following tasks were completed on the EC2 instance.

### Update package list

```bash
sudo apt update
```

### Install Nginx

```bash
sudo apt install nginx -y
```

### Check Nginx status

```bash
sudo systemctl status nginx
```

### Restart Nginx

```bash
sudo systemctl restart nginx
```

### Check disk usage

```bash
df -h
```

### Check memory usage

```bash
free -h
```

### View running processes

```bash
top
```

---

## Task 3 - Website Deployment

A simple HTML page was created containing:

* Name
* College
* Branch
* Email
* Current Date

The default Nginx page was replaced with the custom HTML page.

Default page removed:

```bash
sudo rm /var/www/html/index.nginx-debian.html
```

Custom page copied to:

```text
/var/www/html/index.html
```

The website was successfully accessed using the EC2 Public IP through a web browser.

---

## Task 4 - Git & GitHub

A GitHub repository was created to maintain the project files.

The repository includes:

* index.html
* README.md
* screenshots

Basic Git commands used:

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin <repository-url>
git push -u origin main
```

---

## Bonus Task - Docker

Docker was installed on the EC2 instance.

Installation command:

```bash
sudo apt install docker.io -y
```

Verification:

```bash
sudo docker run hello-world
```

The successful output confirmed that Docker was installed and working correctly.

---

## Folder Structure

```text
aws-devops-intern-assignment/
│
├── index.html
├── README.md
└── screenshots/
    ├── Task-1-EC2/
    ├── Task-2-Linux/
    ├── Task-3-Website/
    ├── Task-4-GitHub/
    └── Bonus/
```

---

## Learning Outcome

Through this assignment, I gained hands-on experience with:

* Launching and configuring an AWS EC2 instance
* Creating Security Groups
* Connecting to a Linux server using SSH
* Installing and managing Nginx
* Deploying a static website
* Using basic Linux administration commands
* Managing source code with Git and GitHub
* Installing and verifying Docker on Ubuntu

---

## Author

**Anant Chaudhary**

GL Bajaj Institute of Technology & Management

Mechanical Engineering

Email: [anant2005ch@gmail.com](mailto:anant2005ch@gmail.com)
