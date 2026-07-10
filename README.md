# Nginx Website Deployment

## Objective

Deploy a simple website on an AWS EC2 Ubuntu instance using Nginx.

---

## AWS Services Used

- Amazon EC2
- Security Groups

---

## EC2 Setup Steps

1. Selected the Ubuntu Server 26.04 LTS as an Amazon Machine Image (AMI).
2.  Used the `t3.micro` instance type.
3. Created a new key pair for SSH access.
4. Configured a Security Group with the following inbound rules:
   - SSH (Port 22) from Admin IP (`49.47.128.114/32`)
   - HTTP (Port 80) from Anywhere (`0.0.0.0/0`)
5. Launched the instance.
6. Connected to the instance using SSH.

---

## Linux Commands Used

### Update packages

```bash
sudo apt update
```

### Install Nginx

```bash
sudo apt install nginx -y
```

### Check Nginx version

```bash
nginx -v
```

### Check Nginx status

```bash
systemctl status nginx
```
---
## Website Deployment

- Created a custom `index.html` page in the Nginx web root (`/var/www/html`).
- Nginx served `index.html` instead of the default `index.nginx-debian.html` because `index.html` has higher priority in the default Nginx configuration (`/etc/nginx/sites-enabled/default`).
- The webpage displays:
  - Name
  - College
  - Branch
  - Email
  - Current Date
---
Website Location:

```text
/var/www/html/index.html
```

## Repository Contents

- index.html
- README.md
