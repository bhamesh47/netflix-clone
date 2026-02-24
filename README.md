Below is a **clean, step-by-step `README.md`** you can **directly use in GitHub** that explains **AWS EC2 instance creation + deploying your Netflix Clone website**.

This is **resume + portfolio ready** and written in **simple, professional language**.

---

## 📄 `README.md` — AWS EC2 Website Deployment (Step-by-Step)

````markdown
# ☁️ AWS EC2 Website Deployment (Netflix Clone)

This project demonstrates **how to create an AWS EC2 instance** and **deploy a static Netflix Clone website** using **Apache Web Server** on **Ubuntu Linux**.

---

## 📌 Objective
- Launch an EC2 instance on AWS
- Configure security groups
- Install Apache web server
- Deploy a static website
- Access the website using a public IP

---

## 🛠️ Tech Stack
- AWS EC2
- Ubuntu 22.04 LTS
- Apache2 Web Server
- HTML & CSS
- Git & GitHub
- Linux (Ubuntu)

---

## 🧾 Prerequisites
- AWS Account
- Basic Linux commands
- GitHub account
- Internet connection

---

## 🚀 Step-by-Step EC2 Instance Creation

### 1️⃣ Login to AWS Console
- Go to https://aws.amazon.com
- Sign in to **AWS Management Console**

---

### 2️⃣ Launch EC2 Instance
1. Open **EC2 Dashboard**
2. Click **Launch Instance**
3. Instance Name: `Netflix-Clone-Server`

---

### 3️⃣ Choose AMI
- Select **Ubuntu Server 22.04 LTS (Free Tier Eligible)**

---

### 4️⃣ Choose Instance Type
- Select `t2.micro` (Free Tier)
- Click **Next**

---

### 5️⃣ Create Key Pair
- Click **Create new key pair**
- Name: `netflix-key`
- Type: RSA
- Format: `.pem`
- Download and save securely

---

### 6️⃣ Configure Network (Security Group)
Allow the following inbound rules:

| Type | Port | Source |
|----|----|----|
| SSH | 22 | My IP |
| HTTP | 80 | Anywhere |
| HTTPS | 443 | Anywhere |

---

### 7️⃣ Launch Instance
- Click **Launch Instance**
- Wait until instance state becomes **Running**

---

## 🔐 Connect to EC2 Instance

### Linux / Mac
```bash
chmod 400 netflix-key.pem
ssh -i netflix-key.pem ubuntu@<EC2-PUBLIC-IP>
````

### Windows (PuTTY)

* Convert `.pem` to `.ppk`
* Connect using Public IP

---

## ⚙️ Server Setup on EC2

### 1️⃣ Update System

```bash
sudo apt update && sudo apt upgrade -y
```

---

### 2️⃣ Install Apache Web Server

```bash
sudo apt install apache2 -y
```

---

### 3️⃣ Start & Enable Apache

```bash
sudo systemctl start apache2
sudo systemctl enable apache2
```

---

### 4️⃣ Verify Apache

Open browser:

```
http://<EC2-PUBLIC-IP>
```

You should see **Apache2 Ubuntu Default Page**.

---

## 📂 Deploy Netflix Clone Website

### 1️⃣ Go to Web Directory

```bash
cd /var/www/html
```

---

### 2️⃣ Remove Default Page

```bash
sudo rm index.html
```

---

### 3️⃣ Upload Website Files

#### Option 1: Using GitHub

```bash
sudo apt install git -y
git clone https://github.com/bhamesh47/netflix-clone.git
sudo cp -r netflix-clone/* /var/www/html/
```

#### Option 2: Manual Upload

* Use SCP / FileZilla

---

### 4️⃣ Restart Apache

```bash
sudo systemctl restart apache2
```

---

## 🌐 Access Website

```
http://<EC2-PUBLIC-IP>
```

🎉 Netflix Clone website is live on AWS EC2!

---

## 📈 Learning Outcomes

* AWS EC2 instance management
* Linux server setup
* Apache web server configuration
* Website deployment on cloud
* GitHub integration

---

## ⚠️ Disclaimer

This project is for **educational purposes only**.
Netflix is a registered trademark of Netflix, Inc.

---

## 👨‍💻 Author

**Bhamesh Megalamani**
GitHub: [https://github.com/bhamesh47](https://github.com/bhamesh47)

---

## ⭐ Support

If you found this useful, please ⭐ the repository!

````

---



