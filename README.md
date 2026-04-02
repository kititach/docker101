# 🚀 Docker 101: Deploy Web ง่ายๆ ด้วย Nginx

## 📌 Overview
โปรเจคนี้สอนตั้งแต่:
- ติดตั้ง Docker
- สร้าง Web (HTML)
- สร้าง Docker Image
- Run Container
- Deploy Web บนเครื่องจริง

---

# 🧱 1. Install Docker

## 🔹 Linux (Ubuntu / Mint)

```bash
sudo apt update 
sudo apt install -y docker.io
```

### เปิดใช้งาน Docker
```bash
sudo systemctl start docker
sudo systemctl enable docker
```

### ตรวจสอบเวอร์ชัน
```bash
docker --version
```
👉 -- = option แบบเต็ม (อ่านง่าย เช่น --help, --version)

## 🔹 ใช้งาน Docker โดยไม่ต้อง sudo
```bash
sudo usermod -aG docker $USER
newgrp docker
```
อธิบาย
- -aG	append (เพิ่มโดยไม่ลบของเดิม) หร้อม ระบุ Group

# 📁 2. Create Project Structure
```bash
mkdir docker-web
cd docker-web

mkdir html
touch html/index.html
touch Dockerfile
```

# 📝 3. Create HTML Page
ไฟล์: html/index.html
```HTML
<!DOCTYPE html>
<html>
<head>
  <title>My Web</title>
</head>
<body>
  <h1>Hello from Docker 🚀</h1>
</body>
</html>
```

# 🐳 4. Create Dockerfile
ไฟล์: Dockerfile
```Dockerfile
FROM nginx:latest

COPY html/index.html /usr/share/nginx/html/index.html
```

# 🔨 5. Build Docker Image
```bash
docker build -t myweb:v1 .
```
อธิบาย
- -t = ตั้งชื่อ image

```bash

```
```bash

```
```bash

```