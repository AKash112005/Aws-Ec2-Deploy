# 🚀 AWS EC2 Frontend Deployment

This project demonstrates how two static frontend websites were deployed on an AWS EC2 instance and managed using Git & GitHub.

---

## 📌 Project Overview

- 🔹 Two static HTML/CSS/JS websites
- 🔹 Hosted on AWS EC2 (t3.micro - Free Tier)
- 🔹 Web server: Apache
- 🔹 Version control using Git
- 🔹 Code hosted on GitHub

---

## 🏗 Architecture Diagram
            +---------------------+
            |      User Browser   |
            |  (HTTP / HTTPS)     |
            +----------+----------+
                       |
                       |
                Public IP Address
                       |
                       |
            +----------v----------+
            |     AWS EC2         |
            |  t3.micro Instance  |
            |---------------------|
            |  Web Server         |
            |  (Nginx / Apache)   |
            |---------------------|
            |  /var/www/html      |
            |   ├── site1         |
            |   └── site2         |
            +----------+----------+
                       |
                       |
            +----------v----------+
            |      EBS Volume     |
            |  (Elastic Block     |
            |   Store - Storage)  |
            +---------------------+
            
---

## 🛠 Technologies Used

- AWS EC2
- Amazon EBS
- Linux (Ubuntu / Amazon Linux)
- Nginx / Apache
- Git
- GitHub

---

## ⚙️ Deployment Steps

### 1️⃣ Launch EC2 Instance

- Instance Type: `t3.micro`
- Open Ports:
  - 22 (SSH)
  - 80 (HTTP)
  - 443 (HTTPS)

---

💰 Cost Optimization
  
    To avoid AWS charges:
    
    Stop instance when not in use
    
    Stay within Free Tier limits (750 hours/month)
    
    Keep EBS under 30GB
    
    Delete unused volumes and snapshots

📈 Future Improvements

    Add HTTPS using Let's Encrypt
    
    Setup CI/CD pipeline
    
    Use GitHub Actions for auto deployment
    
    Move to S3 + CloudFront for static hosting
    
    Add Domain Name with Route 53

👨‍💻 Author

  Akash
  AWS EC2 Deployment Practice Project
