# aws-s3-static-website
Hosted a static website using AWS S3 and CloudFront for global distribution and HTTPS security.
# 🌐 AWS Static Website Hosting Project

## 📖 Overview
This project demonstrates how to **host a static website** using **Amazon S3** and **CloudFront**.  
It’s a beginner-friendly AWS project with **no coding required**, perfect for learning cloud deployment and adding to your resume.

---

## 🪜 Steps to Implement

### 1. Create S3 Bucket
- Created an S3 bucket named `my-portfolio-website-vidyasagar`
- Disabled “Block all public access”
- Enabled **Static website hosting**
- Uploaded 'index.html'

### 2. Configure Permissions
- Added this **bucket policy** for public read access:
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadForWebsiteContent",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::my-portfolio-wedsite-vidyasagar/*"
    }
  ]
}
```

### 3.  Add CloudFront (for HTTPS + Global CDN)

- Go to CloudFront → Create Distribution.
- Under Origin domain, select your S3 bucket.
- Leave default settings for now.
- Scroll down → Click Create Distribution.
- Once status changes to “Deployed”, you’ll get a CloudFront URL

### 4. check your website
- use the url from S3
- open it in your browser
- your webpage will be loaded

### 🧾 Output

🔗 Live Website: Your CloudFront or S3 URL 

🖼️ Screenshots:

<img width="1292" height="818" alt="Screenshot 2025-11-10 120419" src="https://github.com/user-attachments/assets/99cad46e-186c-49bb-980d-35310697a63f" />


<img width="1549" height="758" alt="Screenshot 2025-11-10 120942" src="https://github.com/user-attachments/assets/5899bc63-3231-49f6-ac97-8ea381ab0ef9" />


<img width="1636" height="820" alt="Screenshot 2025-11-10 120827" src="https://github.com/user-attachments/assets/88857a7c-0a4f-4fc2-aff5-dbc6623c74d2" />


<img width="1647" height="817" alt="Screenshot 2025-11-10 120619" src="https://github.com/user-attachments/assets/c19ce3e8-e9da-4241-ac66-d7f549e24a74" />




<img width="1912" height="970" alt="Screenshot 2025-11-10 120007" src="https://github.com/user-attachments/assets/392fbe23-dff6-4978-b635-ae40d75e25df" />











### 🧰 Tools & Services Used
- Amazon S3 — Static website hosting
- Amazon CloudFront — CDN & HTTPS
