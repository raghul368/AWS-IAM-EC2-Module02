# AWS IAM & EC2 – Module 02 Project

A beginner project page for the Codomax Digital Solutions AWS Cloud & DevOps internship.

## Files
- `index.html` — responsive project website (HTML and CSS are included in one file).

## Run locally
Open `index.html` in a web browser.

## Deploy on Amazon EC2 (Amazon Linux 2023)
1. Launch an EC2 instance.
2. In its security group, allow HTTP (TCP port 80) from the required audience. For a public demo, HTTP may be opened to `0.0.0.0/0`.
3. Allow SSH (TCP port 22) only from your own trusted IP address, or use EC2 Instance Connect.
4. Connect to the instance and run:

```bash
sudo dnf update -y
sudo dnf install httpd -y
sudo systemctl enable --now httpd
```

5. Copy `index.html` to the web server document root:

```bash
sudo cp index.html /var/www/html/index.html
```

6. Open `http://YOUR_EC2_PUBLIC_IP` in your browser.

Replace `YOUR_EC2_PUBLIC_IP` with the public IPv4 address shown for your running instance.

## Important
This repository contains a sample project website. It does not create AWS IAM users, policies, EC2 instances, or a live deployment automatically. Perform and verify those tasks in your own AWS account. Never commit private keys, passwords, access keys, or other secrets to GitHub.
