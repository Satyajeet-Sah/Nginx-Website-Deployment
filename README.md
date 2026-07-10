# Nginx-Website-Deployment

## Objective

Deploy a simple website on an AWS EC2 Ubuntu instance using Nginx.

---

## AWS Services Used

- Amazon EC2
- Security Groups

---

## EC2 Setup

1. Launched an Ubuntu EC2 instance.
2. Created a Security Group.
3. Allowed inbound ports:
   - SSH (22)
   - HTTP (80)
4. Connected to the instance using SSH.

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

## Website Deployment

- Replaced the default Nginx page.
- Hosted a custom HTML page containing:
  - Name
  - College
  - Branch
  - Email
  - Current Date

Website Location:

```text
/var/www/html/index.html
```

## Repository Contents

- index.html
- README.md
